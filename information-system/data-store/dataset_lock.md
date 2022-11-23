---
layout: default
title: Dataset Locks
nav_order: 10
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

## What is a dataset lock?

Datasets in the Data Store can be "locked" to prevent changes to the dataset's data or metadata until it is unlocked.

## What happens when a dataset is locked?

Locked datasets are displayed differently to Data Store users. A locked dataset is indicated by a grey lock icon in the settings and upload tabs.

The locking of a dataset is not just cosmetic, the APIs which grant credentials will enforce this status, responding with an error message in the case of an invalid request, as shown below.

|                           Requesting upload credentials for a locked dataset                            |
| :-----------------------------------------------------------------------------------------------------: |
| <img src="../../assets/images/data_store/dataset_lock/locked_api_error.png" alt="drawing" width="600"/> |

If a dataset is locked, the settings panel will display the locked status, for example:

|                              View of locked Dataset in settings tab                              |
| :----------------------------------------------------------------------------------------------: |
| <img src="../../assets/images/data_store/dataset_lock/lock_icon.PNG" alt="drawing" width="600"/> |

If a dataset is locked, the upload tab will show a customised message:

|                                 View of locked Dataset in upload tab                                 |
| :--------------------------------------------------------------------------------------------------: |
| <img src="../../assets/images/data_store/dataset_lock/upload_locked.PNG" alt="drawing" width="600"/> |

## Who can lock a dataset?

Dataset locks can be applied and removed by users who have administrative access to the dataset. See [access control](/access-control.html){:target="\_blank"} for more information about dataset access.

## How to add or remove a dataset lock

To apply or remove a lock, navigate to the dataset in the Data Store, select the "settings" tab (1), then the "Lock Settings" drop down (2), and finally, "Lock The Dataset" (3).

|                                       Accessing lock controls                                       |
| :-------------------------------------------------------------------------------------------------: |
| <img src="../../assets/images/data_store/dataset_lock/finding_lock.png" alt="drawing" width="600"/> |

A helpful, brief justification must be provided for the lock or unlock action. Your identity (email) and justification will be logged in the dataset's lock history (visible below). As an example of a suitable lock justification is "completed initial round of modelling and outputs finalised".

|                                           Dataset lock history                                            |
| :-------------------------------------------------------------------------------------------------------: |
| <img src="../../assets/images/data_store/dataset_lock/lock_event_history.PNG" alt="drawing" width="600"/> |
