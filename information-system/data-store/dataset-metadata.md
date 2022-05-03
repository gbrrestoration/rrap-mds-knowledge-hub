---
layout: default
title: Dataset metadata
nav_order: 3
grand_parent: Information System
parent: Data store

---
{: .no_toc }
# Dataset metadata
<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

## Metadata
The Data Store will have a minimal dataset metadata record schema using [RO-CRATE](https://w3id.org/ro/crate) as the metadata data file format. The minimal dataset metadata record fields are:

### User entered data fields
{% include_relative user-metadata-fields.md %}

### Generated data fields
{% include_relative generated-metadata-fields.md %}

The metadata fields included in Data Store enables data registration, upload, sharing via the S3 APIs to support current modelling activities in M&DS. Future releases will incrementally add additional capability to capture RRAP M&DS, ISO and Science related metadata for when we need wider data publication.

___