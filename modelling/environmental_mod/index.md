---
layout: default
title: Environmental Modelling
nav_order: 2
has_children: 
grand_parent: RRAP M&DS
parent: Modelling
---

# Environmental Modelling: common inputs & processes

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

The following environmental modelling inputs are common across all ecological models, providing the foundation for environmental forcings that inform ecological responses on The Reef.

To generate long-term climate change projections, **eReefs** and **Relocatable Coastal Model (RECOM)** outputs are currently combined with projected temperature trends from MIROC5 and CMIP6 global ocean models. 

**OceanParcels** is used with the eReefs and RECOM output to generate larval connectivity at the cluster scale, while **CONNIE2** is used to provide connectivity at the whole-of-GBR scale. Outputs from the **SWAN** wave model are used to provide wave stress estimates. These environmental models are combined to force ecological models at different spatial scales: 
- Site scale (~250 m),
- Reef cluster scale (<50 km)
- Regional scale across 3806 reefs in the GBR

We are working towards incorporating more integrated downscaled models that capture climate change impacts on ocean currents and eddy processes.

![Figure1](../../assets/images/modelling/common_inputs_figure_1.png)
***Figure 1.** The spatial extent of the 4km resolution eReefs environmental model, showing simulated currents. Top right: Thermal stress (Degree Heating Weeks) from a RECOM model nested within the GBR-scale model to provide higher resolution information for the Moore Reef Cluster. Bottom right: Larval connectivity within the Moore Reef Cluster; arrows show connections where at least one larvae from the source site reached the receiving site.*

## eReefs Suite

The eReefs modelling system (Steven et al., 2019) uses the CSIRO Environmental Modelling Suite (Baird et al., 2020) to represent the 3 dimensional hydro-dynamic, sediment and biogeochemistry and ecological processes to simulate temperature, salinity and water quality across the Reef. 

eReefs hydrodynamic models provide information about currents and water temperature on the Reef in three dimensions and with 1-4 km resolution. eReefs models operate in near real time, allowing current conditions to be estimated, and hindcasts date back to 2010 (4 km grid) and 2014 (1 km grid).

eReefs is a platform that provides a picture of what is currently happening on the reef, and what will likely happen in the future. 

**More information on eReefs:** [CSIRO website](https://research.csiro.au/ereefs/){:target="\_blank"}

### Relocatable Coastal Model (RECOM)

RECOM nests within the larger eReefs models to provide more detail at reef and cluster scales, including local-scale variations in heat stress and currents (Steven et al., 2019).

RECOM models recently delivered environmental input layers for heat stress and connectivity for business-case studies in two reef clusters in the Cairns region (Moore and Hastings) and a reef cluster in the Whitsundays region (Brick).

**More information on RECOM:** [CSIRO website](https://research.csiro.au/ereefs/models/models-about/recom/){:target="\_blank"}

## OceanParcels

OceanParcels (Delandmeter and Seville, 2019) takes output from hydrodynamic models (in this case, the eReefs and RECOM models) as input for a particle-tracking model that we use to calculate coral larval connectivity – that is, the probability that larvae released at one site will reach another site. 

OceanParcels is used to provide connectivity matrices for **C~scape** and **ADRIAmod** at the reef cluster scale. As well as providing data layers for the cluster-scale ecological models, OceanParcels has been used to identify robust source and sink locations for coral larvae within each cluster. 

**More information on OceanParcels:** [Website](https://oceanparcels.org/){:target="\_blank"}

![Figure2](../../assets/images/modelling/common_inputs_figure_2.png)
***Figure 2.** Habitat map of reef sites. Highlighted in orange are sites that consistently act as local sources (left) and settling or destination sites (right) across all three spawning days in all three years.*

## CONNIE2
TODO

## SWAN
TODO

# References

Baird, M.E., Wild-Allen, K.A., Parslow, J., Mongin, M., Robson, B., Skerratt, J., Rizwi, F., Soja-Woźniak, M., Jones, E., Herzfeld, M. and Margvelashvili, N., 2020. CSIRO Environmental Modelling Suite (EMS): scientific description of the optical and biogeochemical models (vB3p0). Geoscientific Model Development, 13(9), pp.4503-4553. [Read Here](https://www.eprints.qut.edu.au/174674/8/Baird_et_al_2020_Geosci_Model_Dev.pdf)

Delandmeter, P. and Van Sebille, E., 2019. The Parcels v2. 0 Lagrangian framework: new field interpolation schemes. Geoscientific Model Development, 12(8), pp.3571-3584. [Read Here](https://gmd.copernicus.org/articles/12/3571/2019/)

Steven, A.D., Baird, M.E., Brinkman, R., Car, N.J., Cox, S.J., Herzfeld, M., Hodge, J., Jones, E., King, E., Margvelashvili, N. and Robillot, C., 2019. eReefs: An operational information system for managing the Great Barrier Reef. Journal of Operational Oceanography, 12(sup2), pp.S12-S28. [Read Here](https://www.tandfonline.com/doi/full/10.1080/1755876X.2019.1650589)