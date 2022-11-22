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

Datasets in the datastore can be locked to prevent any changes from being made to the dataset's data or metadata until it is unlocked. 

Locking is facilitated in the UI by disabling the upload feature and is indicated by a grey lock icon in the settings and upload tabs. The API facilitates locking by responding to update/upload requests with an error message.

Dataset locks can be applied/removed by users who have administration access privileges to the dataset. 

| View of locked Dataset in settings tab |
|:-:|
|<img src="../../assets/images/data_store/dataset_lock/lock_icon.PNG" alt="drawing" width="600"/>|

| View of locked Dataset in upload tab |
|:-:|
|<img src="../../assets/images/data_store/dataset_lock/upload_locked.PNG" alt="drawing" width="600"/>|



## How to add a dataset lock

The dataset lock is only available (and visible) to those with admin privileges over the dataset. To apply/remove a lock, navigate to the dataset in the datastore, select the "settings" tab, then the "Lock Settings" drop down, and finally, "Lock The Dataset". 

A brief and useful reason can be provided and will be logged in the datasets lock history trace which is also visible below. As an example, a lock message might be "completed initial round of modelling and outputs settled". 

| Dataset lock history |
|:-:|
|<img src="../../assets/assets/images/data_store/dataset_lock/lock_event_history.PNG" alt="drawing" width="600"/>|
