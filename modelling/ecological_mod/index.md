---
layout: default
title: Ecological Modelling
nav_order: 3
grand_parent: RRAP M&DS
parent: Modelling
---
{: .no_toc }

# Ecological Modelling

<details  open markdown="block">
  <summary>
    Table of contents
  </summary>
{: .text-delta }
* TOC
{:toc}
____
</details>

## ADRIAMod
TODO

## CoCoNet
The CoCoNet (Coral Community Network) model was developed to explore the role of physical and ecological processes in controlling the health of coral reef systems over both historical periods and future projections. This includes understanding reef futures under different climate scenarios (Condie & Porobic, 2023). In addition, the computational efficiency of CoCoNet supports large ensemble runs that can be used to rigorously estimate model uncertainty. 

CoCoNet is a meta-community model that includes communities of corals and age-structured CoTS populations distributed across a network of 3806 reefs (Figure 1). 

Within the Coral Community Network each reef has a fixed coral carrying capacity proportional to the area of the reef. Coral communities consist of five coral groups whose species are relatively abundant on the GBR:
- Staghorn Acropora 
- Tabular Acropora 
- Montipora
- Poritidae
- Favids

These groups are distinguished within the model in terms of their growth rates, preference by CoTS, and susceptibility to environmental impacts such as cyclones and marine heatwaves. Differences in fecundity among coral groups are assumed to be negligible compared with differences in environmental susceptibility and independent of geographical location along the GBR.

For further detail on the aspects of CoCoNet, its calibration and user guide please refer to the following resources Condie et al. (2018), Condie et al. (2021), Condie & Porobic, (2023).

![Figure11](../../assets/images/modelling/coconet_figure_11.png)

***Figure 1.** Composite image of key CoCoNet components, including environmental forcing, ecological components, and processes (Condie & Porobic, 2023).*

## C~scape
C-scape is a modeling framework specifically designed to integrate information about the key processes that exhibit variability within coral reefs and exert an impact on the growth of coral populations. Its purpose is to forecast the dynamics of coral populations across reef complexes. C-scape's adaptability extends to either a solitary reef or a cluster of small reefs covering a selected geographic region, typically spanning from 10 to 40 kilometers in width.

## ReefMod
ReefMod-GBR is a coral metapopulation model that simulates the key demographic processes of corals (reproduction, dispersal, settlement, growth and mortality) and spatially-realistic stressors (water quality, crown-of-thorns starfish outbreaks, cyclones and bleaching) across 3,806 reefs of the GBR (Bozec et al., 2022) (Figure 2). 

A key feature of the model is that corals are modelled as individual colonies distributed over a spatially-explicit reef surface composed of patches of sand, hard substrates and algae. Six morphological groups of corals are simulated with vital rates derived from GBR field studies and experiments. By simulating realistic coral demographics and disturbance impacts, the model provides a credible reconstruction of recent coral trajectories observed across the GBR (Bozec et al., 2022).

![Figure10](../../assets/images/modelling/reefmod_figure_10.png)

***Figure 2.** Schematic representation of the reef ecosystem model applied to the Great Barrier Reef (ReefMod-GBR). **(A)** Each of the 3,806 individual reefs is represented by a 20x20m horizontal space vertically colonized by coral colonies belonging to six morphological groups. **(B)** Demographic processes (solid arrows) and ecological interactions (dashed arrows) affecting coral colonies individually. **(C)** Modelling of crown-of-thorns starfish (CoTS) cohorts subject to size-specific survival during their life. For both corals and CoTS, settlement occurs from a pool of larvae that results from the retention of locally produced offspring (self-supply) and the incoming of larvae from connected reef populations (external supply) (Bozec et al., 2022).*

# References

Bozec, Y. M., K. Hock, R. A. B. Mason, M. E. Baird, C. Castro-Sanguino, S. A. Condie, M. Puotinen, A. Thompson, and Mumby, P. J., 2022. Cumulative impacts across Australia’s Great Barrier Reef: A mechanistic evaluation. bioRxiv:1–37. [Read Here](https://esajournals.onlinelibrary.wiley.com/doi/epdf/10.1002/ecm.1494)

Condie, S; Plagányi-Lloyd, E.; Morello, B.; Hock, K.; Beeden, R., 2018. Great Barrier Reef recovery through multiple interventions. Conservation Biology. 32(6):1356-1367. [Read Here](https://doi.org/10.1111/cobi.13161)

Condie, S.A., Porobic, J., 2023. Coral Community Network (CoCoNet) Model: User Guide &Technical 
Description. CSIRO, Australia. [Read Here](https://doi.org/10.25919/75v0-2j98)

Condie, S.; Anthony, K.R.N.; Babcock, R.; Baird, M., Beedon, R.; Fletcher, C., Gorton, R., Harrison, D., Hobday, A.J., Plagányi, E.E., Westcott, D.A., 2021. Large-scale interventions may delay decline of the Great Barrier Reef. Royal Society Open Science. 8(4):1-27. [Read Here](https://doi.org/10.1098/rsos.201296)