---
layout: default
title: Registering and uploading a dataset
nav_order: 1
grand_parent: Information System
parent: Data store

---
{: .no_toc }
# Registering and uploading a dataset
<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

## Overview

The diagram below outlines the steps undertaken when registering and uploading a dataset.  
*Note: draft figure*

![Workflow digram](../../assets/images/DRAFTv2_upload_data.png)
*A User logs into the RRAP information system & selects DATASETS then ADD DATASET from the website.  A metadata form prefilled with the User’s name & email address opens and the User fills out information relating to the data being uploaded (see [Filling out form fields](#filling-out-form-fields) for more detailed information). After the metadata form is completed the User uploads the dataset by one of [two methods](#how-do-i-upload-dataset-files), depending on the size of the file(s). The data is assigned its own unique PID (Persistent Identifier).  The data is securely stored on an AWS S3 server and ready for future reference.*
<br>

## Registering a dataset
When registering a dataset with the RRAP-IS Data Store you are initially required to complete a metadata record. The inputs request are listed below, make sure you have these prior to filling out the form. After submitting, the system generates a persistent unique identifier that can be used similarly to a Digital Object Identifier (DOI).  The generation of metadata records will facilitate the sharing and discovery of data.
### Filling out form fields
Mandatory fields are denoted by an astrix (*)
- Author
    - Name*
    - Email*
    - Orcid
- Publisher
    - Organisation*
    - Research Organisation Registry ID
- Dataset
    - Dataset name*
    - Dataset description*
    - Publish date [autofilled]
    - Usage license *
    - Dataset files
- Keywords

### Missing fields
After clicking 'Submit' if a mandatory field is not given a popup will appear indicating that important information is missing.<br>
Users will not be able to progress unless all reqired fields are entered.

### Usage licence

TODO a dropdown list will be provided.  Users can just select the appropreiate licence 

### What happens during the minting dataset process?
TO TO


### Maximum file size

## How do I upload dataset files?
{% include notes.html content="You will require a RRAP-IS AWS account to be able to upload data to the AWS S3 data store." %}

After clicking ***Submit*** button a form will appear that lists the steps for uploading your data. There are currently two options to complete this task.

>> **Upload data via AWS Web Console** -
>> If your dataset is not too large (<1-5GB) and you would like to use a GUI to upload your data, you can upload data using the AWS web interface.

>> **Upload data via AWS Command Line Interface (CLI)** -
>>If your dataset is large (>1-5GB) and/or you would prefer to use the AWS CLI to upload your data steps for this are listed on the form after submitting.

