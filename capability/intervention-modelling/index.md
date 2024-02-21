---
layout: default
title: Reef Interventions
nav_order: 4
has_children: 
grand_parent: RRAP M&DS
parent: Capability
---
# Intervention Modelling

The MDS suite is a collaborative set of environmental, ecological, and economic models working within a decision-support framework. Climate models force the environmental and ecological layers, and influence intervention scope and effectiveness. Scenario analyses of ecological and economic outcomes feedback to inform which intervention strategies and tactics are effective, safe, and robust (Figure 1).

Part of the Decision Support value proposition is the idea that MDS can identify the best location to undertake RRAP interventions, in identifying locations that will help maximise the likelihood that RRAP actions will deliver benefits, and/or identify locations that will maximise the magnitude of those benefits. Combinations of environmental, ecological, social, and economic drivers are used within the MDS suite to construct selection criteria and objectives that inform intervention deployment, option construction and portfolio studies. 

This involves a set of nested spatial scales, spanning subregions (100 - 300 km), reef clusters (10 - 30 km), reefs (1-10 km), sites (100 m) and coral seeding densities (1 – 10 m) and includes the following criteria: 
- cluster selection, 
- reef selection,
- site selection and 
- deployment selection. 

Further information on the processes, systems and decisions used to produce intervention models for RRAP are documented in MDS 2022 Intervention Modelling Report (Adaptus et al., 2022).

![Figure1](intervention_figure_7.png)
*Figure 1. Schematic representation of Modelling and Decision Support (MDS) intervention modelling workflow.*

MDS is working towards an operational product for the RRAP Modelling and Decision Support suite by mid-2024. At first, this will consist of the existing environmental, ecological and economics modelling suite linked via ADRIA to provide tactical intervention-deployment advice and guidance principles (Figure 2). 

The suite will be tailored to analysts with communication products developed from synoptic data. Sequentially, the suite will increasingly allow a broader user community to engage.

![Figure2](intervention_figure_8.png)
*Figure 2. Schematic representation of the Modelling and Decision Support operational model for Reef interventions*

#### Current Priority - Identifying robust strategic and tactical RRAP intervention options in space and time under climate change and deep uncertainty

#### Current Priority - Identifying robust strategic and tactical RRAP intervention options in space and time under climate change and deep uncertainty.

## Regional Scale
The MDS coral models Reefmod (UQ) and CoCoNet (CSIRO) are the data engines for coral dynamics at the GBR scale, both simulating ecological responses to changing environmental conditions and proposed interventions. [**Reefmod**](/rrap-mds-knowledge-hub/modelling/reefmod/ "Reefmod Model") resolves coral metapopulation processes down to the very fine scale of individual coral colonies. Whereas [**CoCoNet**](/rrap-mds-knowledge-hub/modelling/coconet/ "CoCoNet Model") simulates metapopulations at the broader site scale (~10ha), emphasising trophic interactions with CoTS and reef fish.

## Reef Scale
MDS has single model called C~scape that captures processes at the within reefs- scale. It links coral colony growth and survival to population-level responses and to physical and environmental spatial layers, creating a seascape of coral populations. The coral life cycle informed by demographic data is the engine for coral growth. It allows us to investigate interventions that influence different coral life stages (Figure 3).

![Figure3](intervention_figure_9.png)
*Schematic representation of the C~scape framework. C~scape is applied to a reef or cluster of reefs. The reef(s) are divided into units for modelling, referred to as sites. These sites are assigned a carrying capacity which specifies the maximum percentage cover of coral in a polygon, this modulates population growth as coral cover approaches the carrying capacity. The sites have different depths, influencing the populations' exposure to temperature stress. Wave exposure is not fully incorporated but is under development. The C~scape framework incorporates thermal stress variability and connectivity between site population polygons as additional spatial inputs, obtained using the eReefs RECOM model. Each of the sites is initialised with a population of corals consisting of different sizes. The engine driving population growth is an integral projection model (IPM) that describes the coral life cycle, enabling us to project changes in each population of corals over an annual period from time t to time t+1. The simulated transport of coral larvae connects populations.*

## Deployment Risk
MDS analysts seek to explore, in collaboration with environmental managers and decision-makers, the projected net benefits and risks for the Reef and people under a multitude of intervention scenarios within a multitude of environmental scenarios. We have produced a risk-analysis framework for intervention risk on the basis of potential risks triggered by deployment of RRAP technologies (i.e., risk of reduced coral community diversity resulting from the introduction of enhanced coral species). 

The MDS suite employs scenario analyses to simulate and evaluate the risk associated with RRAP interventions. These assessments encompass factors such as the type of intervention technology, deployment location (spanning regional, reef, cluster, and site scales), temporal considerations, and metrics. Metrics include both the benefit (i.e., increased regional live coral cover) and the risk (i.e., diminished functional diversity). 
This powerful and transparent approach will provide Reef managers and decision makers new quality insight into the opportunities, constraints, risks, and potential trade-offs needed to deliver time critical RRAP outcomes transparently in an uncertain future.

The MDS subprogram is working closely with the RRAP Intervention Risk Review Group (IRRG) to ensure the requirements of risk characterisation are addressed according to materiality/priority. 

- [**RRAP Intervention Risk Review Group**](https://gbrrestoration.org/our-team/advisory-and-working-groups/intervention-risk-review-group/)

#### Current Priority - Understanding intervention risks and identifying paths to intervention risk management.

## Economic Evaluation
Continuous performance indices (0-1) Reef Tourism Index (RTI), Reef Fisheries Index (RTI) and Reef Condition Index (RCI) are close to being operational. However, RCI underpins non-use benefit valuations and has been the focus of economic analyses within MDS to date. RCI is comprised of between 3 and 6 metrics, depending on the ecological model, these include: coral cover, coral group diversity, structural complexity, juvenile coral abundance, CoTS cover, and proportion of reef covered by rubble. Further details can be found in MDS 2022 Interventions Modelling Report (Adaptus et a., 2022). 

The MDS subprogram applies two common approaches to assessing economic impacts of reef restoration and adaptation interventions, Cost-Benefit Analysis (CBA) and regional Economic Impact Analysis (EIA). While an EIA provides information on how policy interventions affect regional economic activity, a social CBA generates information on gains or losses in net social benefit and their distribution across different segments of society. 

Economic benefit functions combine non-monetary spatiotemporal benefit functions (i.e., RCI) with updated economic value of benefits estimated in monetary terms. This establishes the link between RRAP intervention outcomes to changes in economic value of benefits enjoyed by people. The economic value of benefits of RRAP intervention inputs and outputs are measured by metrics of regional economic activity and in terms of social surplus, respectively (Adaptus et al., 2022).

### Capability Advancements - updated October 2023
#### Regional Scale
- CoCoNet representation of ocean acidification impacts on corals has expanded (while acknowledging significant ongoing uncertainties).
- Enhanced resolution of coral populations from whole-reef to individual CoTS control sites covering approximately 8 ha of hard substrate suitable for coral growth in CoCoNet (Roelfsema et al. 2021); 
- CoCoNet adoption of MIROC5 climate forecasts (Mehta et al. 2018)
- Improved representation of reef connectivity in CoCoNet by using eReefs GBR1 outputs to update dispersal kernels and RECOM high resolution hydrodynamics to estimate relative retention rates based on reef characteristics.
- Software implementation of ReefMod has been renamed the ‘ReefMod Engine’ (RME). The software has been extensively validated against the native implementation of ReefMod, with outputs of both implementations being numerically identical but 60 times faster for the RME. It is fully documented in a 55 pages document: [**here**](https://www.marinespatialecologylab.org/reefmod-emulator)
- New functionalities for simulating the deployments of corals in RME, including more flexibility in selecting reefs based on their size and the amount of corals available for deployment, in designing sites for deployments within a reef, and for tracking restoration benefits at different spatial scales (site/reef/region). 
- RME runs on Windows and Linux platforms and has been successfully deployed on the HPC (>100,000 model runs). 
•	Operational integration of RME with ADRIA for an extended and informed exploration of restoration benefits. Ecosystem metrics (shelter volumes) have been added to the list of the RME outputs to improve economic valuation. 
- Undertaking efforts to refine the genetic model of coral adaptation implemented in ReefMod.
- Knowledge generated from ReefMod is now quickly available through a new implementation in the RME; the new software is a line-for-line re-implementation of ReefMod in the c++ language, replicating exactly its behaviour and ecological predictions while running ~60 times faster.
- Implemented the RME as a library that can be used by other programming environments for configurating and running ReefMod simulations; the library is currently used in the Intervention study and has been successfully linked to ADRIA.
- RME GUI which is an interactive representation of ReefMod Engine for intervention exploration has been updated. 
- Undertaken a comparative analysis of reef health indicators produced by ReefMod and GBRMPA; this comparison has improved our ability to predict stress exposure, recovery potential and reef resilience for the prioritisation of conventional management interventions.
- Delivered advances in the science and processes behind ReefMod generated results (counterfactual simulations under CMIP-6 projections, intervention simulations and genetic adaptation).
- Updated ReefMod model with effects of suspended sediments
- Delivered particle tracks for the entire GBR (using the GBR1 model) and individual reefs (using nested RECOM models). Products have been made available through the RRAP Information System.
- Undertaken efforts to update the GBR-wide model with inter-individual (within coral group) variability of heat tolerance.
- Revisited the definition of 3D coral realestate for > 3,800 reefs based on the last updated habitat maps; this has produced more accurate estimates of reef areas and coral carrying capacities for integration across the MDS.

#### Reef Scale
- C~scape developed an operational reef ecosystem site-scale modelling capability, which provides greater resolution of knowledge into key counterfactual and intervention decision-making processes. 
- C~scape accelerated uptake of newly generated field and experimental observations through strong subprogram collaborations with EcoRRAP and ECT.
- Improved sensitivity to spatial differences in thermal stress by a new approach to reef sites clustering in C~scape that optimises site size and maximises the depth gradient representativity. 
- Developed new approach for the calculation and implementation of carrying capacity derived from benthic habitat maps to provide a more accurate variability between sites.
- Identified 3 new priority reef clusters that have associated ecological data that will be used to further test and improve the models. Site polygons were generated for these new clusters and provided to the connectivity sub-team to provide high resolution connectivity for these new clusters.  
- Using long-term monitoring data from the Moore reef cluster to validate, the model reproduces observed recovery rates at different reef scales adequately.  
- C~scape model architecture optimised to increase run speed by 150%.
- Population models extended to 5 functional types. Commenced design to integrate genetic outputs into C~scape model.
- MDS simulates the deployment of between 200,000 and 10 million juvenile corals raised in aquaculture on settling devices, distributed onto multiple reefs and sites in the Reef network. Coral growth, survival and recruitment is modelled for all life stages for two (C~scape) to six (ReefMod) coral groups.

#### Economic Evaluation
- Development of methodologies for cost-benefit analyses for interventions. 
- Development of Economic Impact Assessment framework for interventions. 
- Translation functions between ecological metrics and ecosystem services. 
- Steps towards mechanistic models for how corals underpin reef biodiversity with a view to developing biodiversity credits.
___
Adaptus, CSIRO, AIMS, UQ, QUT, R&Z Consulting., 2022. 2021 Intervention Modelling Report – Modelling & Decision Support (MDS) Subprogram. Reef Restoration and Adaptation Program, Version 1.0. Unpublished. Submitted April 2022.

Mehta, V.M., Mendoza, K. & Wang, H. Predictability of phases and magnitudes of natural decadal climate variability phenomena in CMIP5 experiments with the UKMO HadCM3, GFDL-CM2.1, NCAR-CCSM4, and MIROC5 global earth system models. Clim Dyn 52, 3255–3275 (2019). https://doi.org/10.1007/s00382-018-4321-1 

Roelfsema, Chris M., Mitchell B. Lyons, Carolina Castro-Sanguino, Eva M. Kovacs, David Callaghan, Magnus Wettle, Kathryn Markey, Rodney Borrego-Acevedo, Paul Tudman, Meredith Roe, and et al. 2021. "How Much Shallow Coral Habitat Is There on the Great Barrier Reef?" Remote Sensing 13, no. 21: 4343. https://doi.org/10.3390/rs13214343 