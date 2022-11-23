---
layout: default
title: Uploading a dataset
nav_order: 5
grand_parent: Information System
parent: Data store
---

{: .no_toc }

# Uploading a dataset

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

## Overview of the process

The diagram below outlines the steps undertaken when registering and uploading a dataset.  
_Note: draft figure_

![Workflow diagram](../../assets/images/DRAFTv2_upload_data.png)
_A User logs into the RRAP information system & selects DATASTORE then REGISTER DATASET from the website. A metadata form prefilled with the User’s name & email address opens and the User fills out information relating to the data being uploaded (see [Filling out form fields](#filling-out-form-fields){:target="\_blank"} for more detailed information). After the metadata form is completed the User uploads the dataset by one of these [methods](#how-do-i-upload-dataset-files){:target="\_blank"}, depending on the size of the file(s). The data is assigned its own unique PID (Persistent Identifier). The data is securely stored on an AWS S3 server, ready for future reference and usage._
<br>

___
## Uploading dataset files

{% include notes.html content="You will require a set of RRAP-IS AWS credentials to be able to upload data to the AWS S3 data store.  See details on the dataset metadata page obtaining AWS credentials." %}

Dataset files can be uploaded once the metadata record is created. Users can choose between using a GUI or command line. The AWS web console (GUI) can be used for files/folders up to 5GB in size. Larger files should be uploaded using a program like WinSCP or the AWS CLI v2.  
___
### Uploading data via AWS Web Console (small to medium files)
Click on the **Upload data** tab.


Request credentials by clicking the **Request Credentials** button. 


|                                 Uploading small to medium files                          |
| :---------------------------------------------------------------------------------:      |
| <img src="../../assets/images/data_store/uploadSmallMediumFilesStep1.png" alt="drawing" width="600"/> |

Next, open the link to AWS system, by either clicking on the **Click to open storage location** button or the link in the text. Users will then be taken to the AWS S3 bucket location which will house the dataset files. The associated metadata record will be seen as a ro-create-meatadata.json file.  


|                                Uploading small to medium files                          |
| :---------------------------------------------------------------------------------:      |
| <img src="../../assets/images/data_store/uploadSmallMediumFilesStep2.png" alt="drawing" width="600"/> |


In the AWS envrionment: 
* Click the orange **Upload** button.
* Click on **Add files** or **Add folder** depending on what you want to upload. Nagivate to where the files are in your system and select them.
* Click OK. The files should appear in the **Files and folders** section in the AWS envrionment.
* Click on the orange **Upload** button at the bottom of the screen to complete the process. 
* Click **Close** to return to the S3 bucket. 
* Close the browser to exit.

Users can add additional files to the dataset by repeating the steps above.

___
### Uploading files  via WinSCP
If users would prefer to use WinSCP to upload files of any size, instructions on how to do this are [here](./WinSCP-data-access.html){:target="\_blank"}.

___
### Uploading files via the AWS Command Line Interface (AWS CLI)
If users would prefer to the AWS CLI to upload files of any size, instructions on how to do this are [here](./AWSCLI-data-access.html){:target="\_blank"}.  

**NOTE**: In order to use the AWS CLI for uploading you will need to install it first. Please see [this page](./setting-up-the-aws-cli.html){:target=\_blank"} for instructions on how to set up the AWS CLI v2 on your system.
