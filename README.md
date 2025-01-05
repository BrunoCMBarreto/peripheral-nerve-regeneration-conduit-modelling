# Peripheral Nerve Conduit Model

This repository contains a report on the process and results of a collaborative modelling project studying peripheral nerve regeneration.

## Purpose:

This report covers the development of a mathematical and computational model of axonal regeneration in nerve guide conduits (NGCs). NGCs are devices used to treat peripheral nerve injuries (PNIs) by providing a suitable path and chemical environment for nerve growth. The goal of this project was to predict how modifications to NGC designs, particularly the inclusion and distribution of nerve growth factors (NGFs), could improve the speed at which axons were expected to regenerate.

### Reference Sources:

As part of this analysis, prior work from several sources was referenced to guide development of the axon regeneration model. In particular, Razetti et al.'s 2018 paper and Borisyuk et al.'s 2019 paper on stochastic axon interactions in a growth setting were used as the basis for the preliminary modelling performed in that paper prior to simulation the effects of growth factor diffusion.

The full citations for these two works are given below and in the report itself.

Razetti A, Medioni C, Malandain G, Besse F, Descombes X (2018) A stochastic framework to model axon interactions within growing neuronal populations. PLoS Comput Biol 14(12): e1006627. https://doi.org/10.1371/journal.pcbi.1006627

R. Borisyuk, et al. Stochasticity and functionality of neural systems: mathematical modelling of axon growth in the spinal cord of tadpole Biosystems, 93 (2008), pp. 101-114

## Methods:

The primary analysis of this report is the effect of the distribution of nerve growth factor on axon growth speed. To determine the relationship between these two factors, this analysis was implemented through both a COMSOL model and a MATLAB growth simulation. In COMSOL, the concentration gradients over time for NGFs in various different conduit designs were obtained through static fluid diffusion simulations. These concentration gradients were then taken into MATLAB and used as part of a stochastic axon growth model that incorporated the current axon state, position in the conduit, and the gradient of growth factor. Based on prior work in this field by Razetti et al., the stochastic model included a model of the random branching behaviors and gradient-seeking behaviors observed in real world analysis. 

For each conduit design, the conduit was modelled as a simple hollow cylinder without internal structural components, due to practical limitations with implementing a different design in an actual surgical setting. The distribution of NGFs was the primary difference between designs, with a uniform design, a wall-concentrated design, and an end-concentrated design being compared directly due to their use in actual nerve regeneration treatments.

## Observations:

From the simulations, this report found that increasing the magnitude of the NGF gradient had a substantial effect on axon growth rates but did not improve the ability of axons to grow in the direction of the distal end of the conduit. To improve growth specifically towards the damaged distal end, the report's simulations found that an end-concentrated design that placed all NGFs at the distal end before diffusion began was the most effective. This conduit design showed the fastest axon growth rates with the highest likelihood of growing in the desired direction.

However, further analysis must still be performed to determine was well these simulations will match reality as the complete set of reactions governing the direction of axon growth is still a topic of ongoing research, thus these simulations may have overlooked an important factor in optimizing conduit designs.