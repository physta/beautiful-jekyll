---
layout: page
title: Tips for calculations
description: Tips for calculations.
---

The calculations of thermal conductivty for different structures and materials
may require specific parameters, constrains, etc., for the calculations of force constants and 
relaxation times.

Here are given some tips derived from selfexperiences to easier 
the calculations of thermal conductivity. 


### Calculation of force constants

For the calculation of force constants it is recomended to use a cubic conventional cell, 
as is better to produce a symmetric supercell for the calculation of the interatomic force constants.

### General calculation of thermal conductivity

The calculation of the thermal conductivity reducing to primitive cell using `--pa` option provides different
results of those obtained without it. For instance, in diamond the calculation using `--pa` provides values 
closer to the experimental ones, while for SiC is the other way. This issue can be caused for the limited 
grid sampling and its direct effect on the number of normal and umklapp processes depending on the cell.

For KCM is highly recommended to use primitive cell.  

### Thermal conductivity on 2D materials

The thermal conductivity from <i> first principles </i> of 2D materials, as graphene or MoS<sub>2</sub>, requires some
considerations:
- On the calculation of force constants it is required to use a large _z_ component in order
to avoid undesired interations of the upper and lower sheet.  
- On the calculation of the thermal conductivity, the value of &kappa; is normalized by the volume of the
supercell, therefore, larger _z_ component will reduce the thermal conductivty. To compare with experiments,
the value of the thermal conductivity &kappa; provided by <i> first principles </i> has to be rescaled 
multiplying by the _z_ value used in the POSCAR and divided by the one reported by experimental data.
