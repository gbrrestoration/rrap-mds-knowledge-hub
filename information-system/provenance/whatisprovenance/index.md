---
layout: default
title: What Is Provenance
nav_order: 2
has_children: false
grand_parent: Information System
parent: Provenance
---
# What is provenance?

## Introduction

"Provenance refers to the sources of information, such as entities and processes, involved in producing or delivering an artifact" [1]. Entities include datasets, It records what processing and datasets were used to create this result. "Provenance answers the questions of why and how the data was produced, as well as where, when and by whom" [2]. 

In the context of modelling and producing data and information to support decisions, capturing provenance in a standardised form enables:
* Traceability and potential reproducibility of data, model runs, results, workflows and decisions
* The building of trust though explicit transparency of processes leading to decisions, and
* Analysis of workflows identifying benefits, risk and optimisation opportunities


## The Provenance Approach in RRAP M&DS

In the RRAP M&DS Information System, the [Prov-O standard, a W3C Recommendation](https://www.w3.org/TR/prov-o/), is used as a conceptual model to capture and support interchange of provenance information in heterogeneous and distributed environments like RRAP M&DS. 

According to PROV-O, provenance is information about entities, activities and agents (i.e. people) involved in producing a piece of data or a thing. The PROV-O core structure describes how these components are related by defining the following four property types: wasGeneratedBy, wasAssociatedWith, wasAttributedTo and used. 

The figure below shows how the RRAP M&DS implements PROV-O to capture provenance information relating to model run workflows and other related information (input data, associated modellers, outputs data, modelling software/processes).


| Provenance model used in M&DS using PROV-O |
|:-:|
|<img src="../../../assets/images/provenance/provenance-abstract-model.jpg" alt="drawing" width="600"/>|


See also:
* [ARDC's guide on Data Provenance](https://ardc.edu.au/resource/data-provenance/)

## Next steps

* [What are entities?](/rrap-mds-knowledge-hub/information-system/provenance/whatisprovenance/what-are-entities.html)
* [Exploring provenance](/rrap-mds-knowledge-hub/information-system/provenance/exploring-provenance/) 

## References

1. W3C, What is Provenance, Sourced from https://www.w3.org/2005/Incubator/prov/wiki/What_Is_Provenance (Accessed 22 November 2022)
2. ARDC, Data Provenance, https://ardc.edu.au/resource/data-provenance/ (Accessed 22 November 2022)
 