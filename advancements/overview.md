---
layout: default
title: Recent Advancements
nav_order: 1
parent: Advancements
grand_parent: RRAP M&DS
---

{: .no_toc }

# Recent Advancements

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

**Lastest update:** August 2023
## Modelling 
Not Reported

## Decision Support
- ADRIA is now on v0.9.0. Development over the past year has focused on new or enhanced capabilities to better support rapid analysis and assessment. 

These improvements have occurred over three (loosely labelled) categories of 
  - (1) functional capability, 
  - (2) outcome assessment, and 
  - (3) analysis and visualisation. 

Highlights of these improvements are detailed further in the subsections below. 
A full list of changes can be found at: [https://github.com/open-AIMS/ADRIA.jl/releases](https://github.com/open-AIMS/ADRIA.jl/releases){:target="\_blank"}.

- (1) Initial capability to run the ADRIA decision simulations in tandem with ReefMod Engine has been developed. This capability is made possible through a Julia package allowing for the potential for dynamic interoperation between ADRIA and ReefMod Engine. In such a use case, ADRIA would inform/indicate preferred intervention deployment locations for each decision point (e.g., yearly, if deployment decisions are to be made yearly), the implications of which can be explored with ReefMod Engine. This capability is offered through a Julia package and could additionally provide interfaces for users of other programming languages such as R or Python.

- (2) ADRIA now has the capability to assess and identify scenario outcomes – the implication of an intervention strategy under a given environmental conditions – which behave similarly (according to a given metric) and group them into clusters. The assessment is not restricted to time series and can be any data series of interest. The governing rules, which lead to a given cluster can then be examined via a process known as Rule Induction. This is illustrated in the next subsection.

- (3) A full feature set of visualisations and analyses have now been incorporated into the ADRIA platform. A more complete overview of capabilities are shown in [https://open-aims.github.io/ADRIA.jl/stable/usage/analysis/](https://open-aims.github.io/ADRIA.jl/stable/usage/analysis/){:target="\_blank"}. A key recently developed feature is Rule Induction, which applies machine learning approaches to quickly identify (“induce”) scenario conditions that must hold true for a given outcome to be realised or experienced. 

## Capability 

### Reef Characterisation and Selection
Not Reported

### Reef Counterfactuals

- The two regional models (ReefMod & CoCoNet) have also delivered broadly consistent counterfactuals based on CMIP-P climate projections. These results demonstrate the sensitivity of reef health projections to climate scenarios, with responses ranging from gradual recovery after 2050 under optimistic climate scenarios to system collapse under pessimistic climate scenarios. 
- The CoCoNet model has been expanded to represent processes such as fish predation on CoTS,ocean acidification, and a minimal realistic representation of natural selection and adaptation.
- Downscaled bleaching projections from the last climate models (CMIP-6) are available for integration across M&DS, including projections of heat stress (degree heating weeks) under five (5) warming scenarios (SSPs).
- An active community of practice has been established for coral connectivity modelling, propagating improvements in modelling approaches and evaluation across RRAP and other GBR modelling teams.
- The local-scale representation of reef habitats in C~scape has been improved with new methodology to incorporate habitat data layers as inputs to the model to better capture coral suitable habitat.
- Cluster-scale connectivity modelling for C~scape and ADRIAmod has been improved, moving from RECOM passive tracers to particle tracking in OceanParcels, which provides more reliable outputs.
- An improved workflow has been developed for cluster-scale DHW and connectivity data layers in C~scape and ADRIAmod, providing a more robust and repeatable process for case studies

### Reef Interventions

**Regional scale deployment**

- CoCoNet representation of ocean acidification impacts on corals has expanded (while acknowledging significant ongoing uncertainties).
- Enhanced resolution of coral populations from whole-reef to individual CoTS control sites covering approximately 8 ha of hard substrate suitable for coral growth in CoCoNet (Roelfsema et al., 2021);
- CoCoNet adoption of MIROC5 climate forecasts (Mehta et al., 2018)
- Improved representation of reef connectivity in CoCoNet by using eReefs GBR1 outputs to update dispersal kernels and RECOM high resolution hydrodynamics to estimate relative retention rates based on reef characteristics.
- Software implementation of ReefMod has been renamed the ReefMod Engine (RME). The software has been extensively validated against the native implementation of ReefMod, with outputs of both implementations being numerically identical but 60 times faster for the RME. It is fully documented in a 55 pages document [https://www.marinespatialecologylab.org/reefmod-emulator](https://www.marinespatialecologylab.org/reefmod-emulator){:target="\_blank"}
- New functionalities for simulating the deployments of corals in RME, including more flexibility in selecting reefs based on their size and the amount of corals available for deployment, in designing sites for deployments within a reef, and for tracking restoration benefits at different spatial scales (site/reef/region). 
- RME runs on Windows and Linux platforms and has been successfully deployed on the HPC (>100,000 model runs). 
- Operational integration of RME with ADRIA for an extended and informed exploration of restoration benefits. Ecosystem metrics (shelter volumes) have been added to the list of the RME outputs to improve economic valuation. 
- Undertaking efforts to refine the genetic model of coral adaptation implemented in ReefMod.
- Knowledge generated from ReefMod is now quickly available through a new implementation in the RME; the new software is a line-for-line re-implementation of ReefMod in the c++ language, replicating exactly its behaviour and ecological predictions while running ~60 times faster.
- Implemented the RME as a library that can be used by other programming environments for configurating and running ReefMod simulations; the library is currently used in the Intervention study and has been successfully linked to ADRIA.
- RME GUI which is an interactive representation of ReefMod Engine for intervention exploration has been updated. 
- Undertaken a comparative analysis of reef health indicators produced by ReefMod and GBRMPA; this comparison has improved our ability to predict stress exposure, recovery potential and reef resilience  for the prioritisation of conventional management interventions.
- Delivered advances in the science and processes behind ReefMod generated results (counterfactual simulations under CMIP-6 projections, intervention simulations and genetic adaptation).
- Updated ReefMod model with effects of suspended sediments
- Delivered particle tracks for the entire GBR (using the GBR1 model) and individual reefs (using nested RECOM models). Products have been made available through the RRAP Information System.
- Undertaken efforts to update the GBR-wide model with inter-individual (within coral group) variability of heat tolerance.
- Revisited the definition of 3D coral realestate for > 3,800 reefs based on the last updated habitat maps; this has produced more accurate estimates of reef areas and coral carrying capacities for integration across the M&DS.

**Reef scale deployment**

- C~scape developed an operational reef ecosystem site-scale modelling capability, which provides greater resolution of knowledge into key counterfactual and intervention decision-making processes. 
- C~scape accelerated uptake of newly generated field and experimental observations through strong subprogram collaborations with EcoRRAP and ECT.
- Improved sensitivity to spatial differences in thermal stress by a new approach to reef sites clustering in C~scape that optimises site size and maximises the depth gradient representativity. 
- Developed new approach for the calculation and implementation of carrying capacity derived from benthic habitat maps to provide a more accurate variability between sites.
- Identified 3 new priority reef clusters that have associated ecological data that will be used to further test and improve the models. Site polygons were generated for these new clusters and provided to the connectivity sub-team to provide high resolution connectivity for these new clusters. 
- Using long-term monitoring data from the Moore reef cluster to validate, the model reproduces observed recovery rates at different reef scales adequately. 
- C~scape model architecture optimised to increase run speed by 150%.
- Population models extended to 5 functional types. Commenced design to integrate genetic outputs into C~scape model.
- M&DS simulates the deployment of between 200,000 and 10 million juvenile corals raised in aquaculture on settling devices, distributed onto multiple reefs and sites in the Reef network. Coral growth, survival and recruitment is modelled for all life stages for two (C~scape) to six (ReefMod) coral groups.

**Risk of deployment**

Not Reported

**Economic valuation and modelling**

- Development of methodologies for cost-benefit analyses for interventions. 
- Development of Economic Impact Assessment framework for interventions. 
- Translation functions between ecological metrics and ecosystem services. 
- Steps towards mechanistic models for how corals underpin reef biodiversity with a view to developing biodiversity credits.

## Information System 

- Released the first version of the M&DS information system, having drawn together coherent specifications for the needs across this complex subprogram (stakeholders, knowledge, systems, processes).
- Documented workflows across modelling and decision support teams to optimise effort in managing internal people, processes & systems within the Modelling and Decision Support suite. [https://miro.com/app/board/uXjVMM9Bg58=/?share_link_id=443926691038](https://miro.com/app/board/uXjVMM9Bg58=/?share_link_id=443926691038){:target="\_blank"}.
- Commenced facilitating user and study-team engagement with the M&DS information system, whilst simultaneously using the process to get user feedback and refine user requirements for the 2nd version due to be released in 2023.
- Information System Release notes v1.3 “Flowerpot Coral” in March 2023 improving:
    - Registry and Data Store search functionality 
    - Minor bug fixes and the UI to the Provenance Store and Registry 
- Information System Release v1.4 “Guitarfish” in May 2023 improving:
    - IS Registry by: (1) Item update history - enables tracking, viewing and reversion to previous iterations of Registry Items and (2) item clone feature - enables the creation of new Registry Item's where the form details are prefilled from an existing item.
    - Data Store by: (1) addition of preferred citation field to inform users how dataset should be cited, (2) addition of ethics and consent, export control and Indigenous Knowledge metadata fields, (3) addition of ethics and consent check in Person item types. 
    - Minor bug fixes and the UI to the Registry and Provenance store
- Improved model integration: 
    - C-scape and ReefMod have a standardised approach for coral available substrate calculations.
    - Improved transfer of information (coral larvae) across scales with a new developed capability to track the origin of larvae from individual reefs (ReefMod) outside the targeted high resolution reef clusters (C~Scape).
    - Two-way workflow between ADRIA and ReefMod: ADRIA can run scenario analyses directly with ReefMod as the model engine, and inform site and reef selection for ReefMod and other models (C~Scape and CoCoNet) 

# References

Mehta, V.M., Mendoza, K., Wang, H. (2019). Predictability of phases and magnitudes of natural decadal climate variability phenomena in CMIP5 experiments with the UKMO HadCM3, GFDL-CM2.1, NCAR-CCSM4, and MIROC5 global earth system models. Climate Dynamics 52, 3255–3275. https://doi.org/10.1007/s00382-018-4321-1 

Roelfsema, Chris M., Mitchell B. Lyons, Carolina Castro-Sanguino, Eva M. Kovacs, David Callaghan, Magnus Wettle, Kathryn Markey, Rodney Borrego-Acevedo, Paul Tudman, Meredith Roe, and et al. (2021). How Much Shallow Coral Habitat Is There on the Great Barrier Reef?. Remote Sensing 13(21), 4343. https://doi.org/10.3390/rs13214343 
