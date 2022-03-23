---
layout: default
title: Registering and uploading a dataset
nav_order: 2
grand_parent: Information System
parent: Data store

---
# Registering and uploading a dataset
## Table of contents
{: .no_toc .text-delta }
* TOC
{:toc}
## Overview

Diagram of the steps and what happens at each step

## Registering a dataset
When registering a dataset with the RRAP-IS Data Store you are initially required to complete a metadata record. The inputs request are listed below, make sure you have these prior to filling out the form. After submitting the system generates a persistent unquie identifier that can be used similarly to a Digital Object Identifier (DOI).  The generation of metadata records will facilitate the sharing and discovery of data.
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
After clicking 'Submit' if a mandatory field is not given a popup will appear indicating a important missing piece of information

#### Usage licence

TODO a dropdown list will be provided.  Users can just select the appropreiate licence 

### What happens during the minting dataset process?

### Maximum file size

## How do I upload dataset files?
After clicking 'Submit' a form will appear that lists the steps for uploading your data. There are currently two options to complete this task.
 {% include note.html content="You will require AWS access to perform a dataset upload." %}

### Upload data via AWS Web Console
If your dataset is not too large (<1-5GB) and you would like to use a GUI to upload your data, you can upload data using the AWS web interface

### Upload data via AWS Command Line Interface (CLI)
If your dataset is large (>1-5GB) and/or you would prefer to use the AWS CLI to upload your data steps for this are listed on the form after submitting.