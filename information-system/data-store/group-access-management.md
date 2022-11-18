---
layout: default
title: Group access management
nav_order: 9
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

Dataset accessibility can be managed by controlling what the general datastore user can do with the dataset, and by controlling which groups can access a dataset, and the extent of their access. This documentation will discuss the latter.

The group access feature enables custom permission for groups (and their members) to a dataset. This facilitates the privatisation of datasets to only certain users of the information system.

This documentation will discus the creation of groups and the setting of configuration of their individual privilidges. 

### Types levels of access

Much like the general user acces (here), there are numerous group access levels charactersed in the same way by:

1. Metadata access (read/write)
2. Data access (read/write)
3. Admin access (lock/unlock)

For individual datasets, groups can be made to achieve the same granularity of access as for general user access, but for a set of members belonging to a group. Further, a dataset can be made available to more than one group with differing accessibility levels. For example, you may wish to have a group of dataset contributors which will require write access, and another group for dataset viewing only, meanwhile the more general system users may not have access at all.



## Creating a group

Group creation is currently performed by information system administrators. Please get in touch and we can facilitate this for you.


## Allowing group access to datasets

If 'Default data store access configuration' in the group creation process, and a user belonging to that group creates a new dataset, then it will automcatically be made available to all group members according to the specified access levels for that group. 

Otherwise, groups access to datasets can also be manaully managed under the 'settings' tab of a dataset.

## Editing group access levels

Upon assigning a group access to a dataset, (whether this was automatically with default levels, or added manually) the access can be changed and customised for this dataset by navigating to the dataset->settings->Access Control->Groups then editing the access for a particular group.