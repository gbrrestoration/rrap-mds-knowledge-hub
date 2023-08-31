---
layout: default
title: Provenance Reporting
nav_order: 5
parent: Information System
grand_parent: RRAP M&DS
---

{: .no_toc }

# RRAP M&DS IS Provenance Reporting

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

To assist in M&DS's ability to report on modelling activities, the [Provena](./index.md) information system has been extended to generate regular CSV reports of modelling activities.

These CSV reports are automatically generated and stored securely each day.

### Accessing Provenance Reports

If the normal ability to view and interrogate Provena provenance is unsufficient, you could talk to your system maintainer and request access to the reports. For now, this will be on a case-by-case basis, but if regular reporting becomes a priority please feel free to raise this issue and regular delivery or direct user access can be considered.

### Understanding Provenance Reports

Provenance reports are exported in a CSV format, including a header row. This makes them suitable for direct ingestion into Excel, or similar tools.

The following columns are included:

-   **Agent (and name/id)**: The Registry Person associated with this Model Run, including additional columns for the Person's Name and ID
-   **Organisation (and name/id)**: The Registry Organisation (optionally) associated with this Model Run, including additional columns for the Organisation's Name and ID
-   **Model (and name/id/version)**: The Registry Model associated with this Model Run (linked through the Model Run Workflow Template), including additional columns for the name, ID and version
-   **Start Time/End Time**: The start/end time of the Model Run, in the timezone specified by the exporter (currently set to AEDT+11:00)
-   **Model Run ID**: The ID of the Model Run
-   **Model Run Template ID**: The ID of the Model Run Workflow Template which this Model Run satisfies
-   **Model Run Description**: The description associated at submission time for this Model RUn
-   **Input ID (and name)**: The ID of the dataset used as input to the model run (if any), including an additional column for the Dataset name
-   **Output ID (and name)**: The ID of the dataset used as output to the model run (if any), including an additional column for the Dataset name
-   **Additional Annotations\***: Model Run's can include additional annotations, as specified in the Model Run Workflow Template. Any annotation from any model run is included as a separate column. If that annotation is not present in other model runs, the cell is empty.

<td>{% include notes.html content="Model Runs can include multiple input/output datasets. In such cases, a single model run will occupy multiple rows, with each row sharing all common column values except the distinct dataset details. The Model Run ID can be used to ensure rows are unique. For example, avoid counting model runs by using the number of rows." %}</td>
