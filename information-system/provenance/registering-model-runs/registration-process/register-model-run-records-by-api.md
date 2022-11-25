---
layout: default
title: Register model run records by API
nav_order: 2
has_children: false
grand_parent: Registering model runs
parent: Creating and registering model run records
---

{: .no_toc }

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

# Register model run records by API

Directly registering model run records by using the Provenance Store [API](https://en.wikipedia.org/wiki/API) is an efficient and scalable approach.

RRAP APIs can be integrated in an automated way into any internet connected computing environment.

See the sections below for information about how to use the API.

## Endpoints and documentation

The RRAP IS APIs are [REST](https://www.redhat.com/en/topics/api/what-is-a-rest-api)ful Python [ASGI](https://asgi.readthedocs.io/en/latest/) compliant services. All APIs exposes two documentation endpoints. The Provenance API documentation is linked below:

-   Provenance Store API
    -   [Swagger](https://swagger.io) documentation - [https://prov-api.rrap-is.com/docs](https://prov-api.rrap-is.com/docs)
    -   [Redoc](https://github.com/Redocly/redoc) documentation - [https://prov-api.rrap-is.com/redoc](https://prov-api.rrap-is.com/redoc)

## Authentication and authorisation

Authentication is provisioned by our [Authentication Server](https://auth.rrap-is.com/auth/realms/rrap/account) and signed using the [JSON Web Token](https://jwt.io/introduction) (JWT) standard.

Sending signed JWTs over an encrypted HTTPS connection is a trusted and secure way to communicate your authorisation.

There are two RRAP IS supported methods of script-ready authentication:

-   [OAuth device auth flow](https://www.oauth.com/oauth2-servers/device-flow/) - this authentication flow is easy and ergonomic to use and is suitable for minimal or even no input environments (such as automated scripts). However, this process requires **intermittent user interaction** to approve the authorisation using a browser on an internet connected device. For more information about using the device auth flow, see TODO.

-   Offline token auth flow - this authentication flow enables authentication for completely automated/[headless](https://en.wikipedia.org/wiki/Headless_computer) scripts. After an initial setup process which involes generating a long lived token, a securely stored token can be reused for a long period of time to access the system. Documentation for this process is a work in progress - TODO.

Regardless of the workflow above, you can make an authenticated API call by including an `Authorization` Header with the value `Bearer <your access token here>`. Each of the APIs expose a set of access check endpoints which enable you to check your access to the API in a predictable way e.g. [check-write-access](https://prov-api.rrap-is.com/docs#/Access%20check/check_write_access).

Authorisation is established by decoding the JWT, verifying the signing signature, and reading the list of roles that your user has been granted. You can check what roles you have access to and request additional access by [logging in](../../../getting-started-is/logging-in) and visiting the [roles view of your profile](https://rrap-is.com/profile?function=roles).

## Example payloads

All RRAP IS APIs use JSON to communicate. This object notation is easy to read for computers and humans.

All endpoints are automatically documented, including example payloads, see [documentation](#endpoints-and-documentation) above.

Below, we will provide some examples of syntactically valid payloads for provenance API endpoints.

The IDs used in these records are not real.

### Model Run Record

```json
{
    "workflow_template_id": "1234",
    "inputs": [
        {
            "dataset_template_id": "1234",
            "dataset_id": "1234",
            "dataset_type": "DATA_STORE",
            "resources": {
                "configuration_file": "data/configuration/config1234.csv"
            }
        }
    ],
    "outputs": [
        {
            "dataset_template_id": "1234",
            "dataset_id": "1234",
            "dataset_type": "DATA_STORE"
        }
    ],
    "annotations": {
        "RCP": "45",
        "species": "speciesA"
    },
    "description": "This model run is not real but is used to demontstrate the model run record payload structure.",
    "associations": {
        "modeller_id": "1234",
        "requesting_organisation_id": "1234"
    },
    "start_time": 1669355820,
    "end_time": 1669442219
}
```

## Example notebooks

To provide end to end examples of common API driven workflows, we have a blog style series of [Python Jupyter Notebooks](https://jupyter.org/).

The blog is available [here](https://gbrrestoration.github.io/rrap-demo-blog/).
