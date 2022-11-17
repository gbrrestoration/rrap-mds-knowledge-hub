---
layout: default
title: General access management
nav_order: 8
grand_parent: Information System
parent: Data store
---

{: .no_toc }

# Managing general user access to a dataset

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

Dataset access control is achieved through group only access, and/or by controlling what the general datastore user can access. This documentation will discuss the latter of controlling what the general datastore user can do with the dataset and will not concern group access to the dataset. See here for information on group access control. 

There are three access rights to consider. 
1. Metadata access 
2. Data access
3. Admin access


## Where to change access control

Update access rights for a registered dataset by navigating to the 'settings' tab when viewing the dataset.

In future versions of the IS, the ability to set access during the registration process will be implemented. For now, a workaround is to register a dataset with meaningless metadata, update access privileges, then meaningfully update the metadata.


## Metadata general access

Facilitates control of metadata viewing and updating by general datastore users.

### Metadata read

If enabled, users will be able view the dataset's metadata and find the dataset in the datastore search and list features. 
If disabled, users will not be able to view the metadata nor find the dataset in the datastore.


#### Metadata Write

If enabled, users can update metadata fields. (Will overwrite the read setting to also grant read access to general users.)
If disabled, general users will not be able to update the metadata.

## Data general access

This allows control over whether general users can upload/download to and from the storage location associated with the dataset. I.e., whether users can access the actual data of the dataset, not just the metadata.  

### Data read

If enabled, the download panel will become visible to general users and they will be able to download data from the storage location. If disabled, the download panel will not be visible and general users will not be able to download data from the storage location.

### Data write

If enabled, users will be able to upload/write/overwrite and download to and from the storage location as both the upload and download panels will be made available to general users.

## Admin access

If enabled, provides administrative control over the dataset. That is, provides all of the above privileges as well as the ability to lock and unlock the dataset. For more information on locking and unlocking, see here.