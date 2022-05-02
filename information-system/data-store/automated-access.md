---
layout: default
title: Automated datastore access
nav_order: 2
grand_parent: Information System
parent: Data store
---

{: .no_toc }

# Automated data store access

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

{% include danger.html content="Be aware that the following guide contains material intended for advanced users of the RRAP M&DS IS data store. This guide will make some assumptions about familiarity with scripting, APIs, authentication etc. If something is unclear, please contact us." %}

## Goals

In order to facilitate data access in automated process such as modelling workflows, data analytics, dashboards etc. the M&DS IS data store is capable of delivering data in a non-interactive (automated/scriptable) manner. We want to be able to:

-   produce a key/secret which provides access to the datastore
-   use this key/secret to get access to the data stores functions
-   apply this process in a non-interactive/scripted workflow

## Prerequisites

As a user of the RRAP M&DS IS, there are some steps you need to take to get automated access setup. Before we start, however, please ensure that you meet the following pre-requisites.

-   You have signed up as a user of the RRAP M&DS IS
-   You have the correct access permissions to download data (see [getting access](../getting-started-is/requesting-access-is.html){:target="\_blank"})
-   You are comfortable using a scripting language which can perform HTTP REST API calls (example code will be provided in [Python](https://www.python.org/){:target="\_blank"} but could be easily transformed into other scripting languages)
-   If you want to use the example scripts, you will need a working [Python](https://www.python.org/){:target="\_blank"} installation (version greater or equal to 3.8 recommended)

## Generating a reusable key

In order to automate access without logging in through a browser, you need to perform the one time process of generating an RRAP M&DS IS API key. This key needs to be kept safe as it provides indiscriminate access to your account permissions. It can be revoked at any time, however, if something does go wrong.

Begin by cloning this [code repository](https://github.com/gbrrestoration/mds-is-client-tools){:target="\_blank"}. The scripts in this repository are written in Python.

The `get_offline_code.py` script can be used to generate your key.

Setup a python virtual environment and install depedencies, on a linux like environment this can be achieved using:

```bash
python3.10 -m venv .venv
source .venv/bin/active
pip install -r requirements.txt
```

noting that the specific python version you use depends on your installation.

On a Windows environment, dependending on how you have installed Python, you should use something like:

```
python -m venv virtual_env
virtual_env\Scripts\activate
pip install -r requirements.txt
```

Once you have installed the dependencies and have a working Python virtual environment, you can run the script:

```bash
python get_offline_code.py
```

The following steps will occur:

-   Initiate an [OAuth2 Device Auth Flow](https://auth0.com/docs/get-started/authentication-and-authorization-flow/device-authorization-flow#:~:text=With%20input%2Dconstrained%20devices%20that,easy%20way%20to%20enter%20text.){:target="\_blank"}.
-   Open a browser (if possible) to the challenge URL address with the code already pre-filled. If this fails, the URL will be presented in the console so you can manually navigate to this URL using another device. It is recommended to run this script in a computing environment where a browser is installed. Once you have recieved the token you can operate in a [headless](https://en.wikipedia.org/wiki/Headless_software){:target="\_blank"} environment.
-   Await your consent at the challenge URL in the browser tab that was opened.
-   Once you confirm access, the offline token will be received from the authorisation server. This token will be output to the console.

## Managing key safely

This API key is essentially a long lived refresh token meaning that it can be exchanged for access tokens with your user permissions on demand. For this reason, it needs to be kept safe.

Always use a secret management approach when including this key in your scripts. Use environment variables or other secret safe methods for utilising the key in your scripts.
https://cloud.google.com/docs/authentication/api-keys#securing_an_api_key

{% include danger.html content="Do not share your key with other users - instead each user should produce their own API key." %}

## Understanding the authentication workflow

The API key you have produced can be used in the following workflow:

-   API key is sent as `refresh_token` to the authorisation refresh token endpoint
-   User receives an `access_token` in response
-   Access token can be used to interact with system APIs for example to
    -   Lookup details of a dataset based on handle ID
    -   Use details to get tailored [AWS access credentials](./setting-up-the-aws-cli.md){:target="\_blank"}
    -   Use credentials to [download](./downloading-datasets.md){:target="\_blank"} contents of dataset
-   To include an `access_token` to system APIs, the `Authorization` header is used with the value `Bearer <your token here>`.

The steps below will cover this process in more detail and provides an automated example of downloading a dataset using the API key.

## Exchanging key for live access token

The script `offline_access.py` provides a function `exchange_offline_for_access` which expects your API key to be present as an [environment variable](https://en.wikipedia.org/wiki/Environment_variable){:target="\_blank"} called `RRAP_OFFLINE_TOKEN`. This function will raise an exception (fail) if this environment variable is not present or if something else goes wrong. 

An example usage (on linux based system):
```bash
export RRAP_OFFLINE_TOKEN="<your token here>"
python offline_access.py
``` 
the output should provide your token to the terminal.

## Using token to access resources




## End to end scripting examples

### Python environment
