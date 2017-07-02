---
layout: page
title: INPUT file 
description: How to define specific inputs.
---

An INPUT file is used by KCM.py to define specific parameters as boundary effects or 
different projections of the thermal conductivity on certain directions.

The INPUT file also allows to specifiy the outputs you want to obtain from the calculations, 
as cumulative thermal conductivity or the thermal conductivity tensor.

An example INPUT file is download together with KCM.py in order to easier the definition of parameters. Use it as reference.

### INPUT parameters

	TEMP= 100 200 300
	BOUNDARY= Y
	TYPE= W
	L= 56e-9
	I_SF= 1
	T_FILE= Y
	K_W= Y
	K_MFP= Y
	TAU_W= Y
	TAU_T= N

See a brief explanation of each parameter:
- `TEMP`. Specify the temperature on which calculations will be carried. Write `ALL` if you want to run the calculation on all the temperatures. The temperatures must correspond
to those calculated in <b>phono3py</b> with the `--ts` option.
- `BOUNDARY`. Specify `Y` or `N` if you want or not include boundary scattering.
- `TYPE`. If considering boundary effects, indicate the type of sample: `W` for wire, `F` for film and `R` for rod.
- `L`. Represents the length of the sample. For a wire L=diameter, for a film L=thickness, and for a rod L=<math><msqrt><mi>A</mi></msqrt></math>, where A is the rod section.


Some times is interesting to observe the effect of increase or decrease the effect of the impurity/mass deffect on the thermal conductivity.
To avoid the need of repeating the calculation of the thermal conductivity, it has been included the option `I_SF` (Impurity Scaling Factor).

