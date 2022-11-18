---
layout: default
title: Access Control
nav_order: 9
grand_parent: Information System
parent: Data store
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

# Overview

This document will initially discuss the types of access controls available, and then reveal the methods to apply these access controls through the Datastore User Interface. Where these controls can be applied for general datastore users (the group of all users), or for smaller customised groups of datastore users.

# What access controls are available for datastore datasets?
 
There are three access rights to consider: 

1. Metadata access
2. Data access
3. Admin access


## Metadata access

Facilitates control of metadata viewing and updating.

### Metadata read

If enabled, users with this right will be able view the dataset's metadata and find the dataset in the datastore search and list features. 
If disabled, users will not be able to find the dataset in the datastore let alone view the metadata.


#### Metadata Write

If enabled, users can update metadata fields and will be granted metadata read access regardless of the setting for metadata read.
If disabled, general users will not be able to update the metadata.

## Data access

Facilitates control over the upload/download of data to/from the storage location associated with the dataset.

### Data read

If enabled, the download panel will become visible to users and they will be able to download data from the storage location. 
If disabled, the download panel will not be visible and users will not be able to download data from the storage location.

### Data write

If enabled, users will be able to upload/write/overwrite and download to/from the storage location as both the upload and download panels will be made available to general users.
If disabled, users will not be able to upload/write/overwrite data in the storage location.

## Admin access

If enabled, provides administrative control over the dataset. That is, the ability to lock and unlock the dataset in addition to all of the above privileges. For more information on locking and unlocking, see here.

# Applying Access Controls

The aforementioned controls can be applied for individual datasets. Each dataset can have a rule for its accessibility to (the group of) general datastore users, and (optionally) extra rules for multiple custom groups of users. The following sections will discuss these. 

Note: If a user is accessing a dataset with access rules for multiple groups of which the user is all apart of, the user will be given the more permissive access rights. This is because enabling an access right is seen as 'granting" action, meanwhile not enabling an access right is *not* seen as 'denying' access. Therefore, roles can only grant access, not deny. 

## General user access to dataset

### Who are general users?

General Datastore users refers to the group of all users who can access the datastore. As such, general user access controls facilitate the general privacy or publicity (to datastore users) of a dataset. It may be a good idea to limit access controls for general users if you wish to keep your dataset private to your team (perhaps during development processes and then later release it by updating general user access rights).

### Where to manage general user access

Upon registering a dataset, the general datastore user access rights can be managed by navigating to the 'settings' tab when viewing the dataset.

In future versions of the IS, the ability to set access during the registration process will be implemented. For now, a workaround is to register a dataset with meaningless metadata, limit general access privileges, then meaningfully update the metadata.

## Group access to dataset

The group access feature enables custom permission for groups (and thus members) to a dataset. This can facilitate the privatisation of datasets to only certain users of the information system.

A dataset can be made available to more than one group with differing accessibility levels. For example, you may wish to have a group of dataset contributors which will require write access, and another group for dataset viewing only, meanwhile the more general system users may not have access at all. 


## Creating a group

Group creation is currently performed by Information System Administrators. Please get in touch and we can help facilitate this for you.


## Allowing group access to datasets

Groups access to datasets can be manually managed under the 'settings' tab of a dataset. Here, groups can be added to dataset access to grant their users read/write permissions to the dataset.

Group access can be automatically applied if 'Default data store access configuration' is enabled in the group creation process by the IS administrator. The result is that if a user belonging to that group creates a new dataset, then it will automatically be made available to all group members according to the specified default access levels for that group. Access levels are individual to a dataset so they can then be customise by following the instructions in the next section.


## Editing group access levels

Upon assigning a group access to a dataset, (whether this was automatically with default levels, or added manually) the access can be changed and customised for this dataset by navigating to the dataset then Settings->Access Control->Groups and selecting a particular group to edit the access levels for this dataset.