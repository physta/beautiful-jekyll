---
layout: page
subtitle: How to use KCM with phono3py
description: How to use the KCM with phono3py output.
---

Here are given the main steps to follow to calculate the thermal conductivity in the KCM
with the phono3py outputs. 

### Phono3py calculation

Download phono3py and follow the instructions given [here](https://atztogo.github.io/phono3py/index.html)
to obtain the force constants for the desired material.

Once you have the FORCES_FC2  FORCES_FC3  FORCE_SETS file execute

    phono3py --dim="2 2 2" --sym_fc3 --sym_fc2 --tsym -c POSCAR

This will provide the harmonic and anharmonic force constants files fc2.hdf5 and fc3.hdf5.

`--dim` corresponds to the cell dimension used to obtain the force constants.

Next, execute your adapted command of this example:

    phono3py --dim="2 2 2" --fc3 --fc2  --pa="0 1/2 1/2 1/2 0 1/2 1/2 1/2 0" -c POSCAR --mesh="20 20 20" --br --nu  --ts="300 400" --isotope --mv="2.01e-4 2.01e-4" -o name

`--fc3` and `--fc2` is used to avoid new calculation of the force constants done in the previous step.

`--pa` is used to reducte to the primitive cell. This reduce the computational time. Here you have to introduce the primitive vectors as done in the example for the FCC structure.

`--br` is used to fast calculation of the relaxation times.

`--nu` is used to split _N_ and _U_ processes. This is necessary to run the KCM calculation.

`--ts` indicates the temperatures to run the calculations.

`--isotope` calculates the natural isotope concentration scattering.

`--mv` indicates the value of the isotope strength. If is not indicated is used natural isotope concentration. Notice that you have to indicate as many values as
atoms you have in the primitive cell (if using `--pa` option) or in the conventional cell according to the POSCAR. 

`-o` is used with an extra `name` to avoid overwirtting of the output file.

This calculation will provide a `kappa-mxxx.hdf5`, where `xxx` is the mesh indicated above.

### KCM calculation

Start by cloning the script 
[KCM.py](https://github.com/physta/kcm/script).

    git clone git://github.com/physta/kcm

To run the KCM calculation execute:

    python KCM.py --pa="0 1/2 1/2 1/2 0 1/2 1/2 1/2 0" POSCAR kappa-mxxx.hdf5

Use only --pa if it was also used in the previous phono3py calculation.

