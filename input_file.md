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

	BOUNDARY= Y
	TYPE= W
	L= 56e-9
	I_SF= 1
	PROJ= Y
	DIR= sin60 0.5 0
	T_FILE= Y
	K_W= Y
	K_MFP= Y
	TAU_W= Y
	TAU_T= N

Some times is interesting to observe the effect of increase or decrease the effect of the impurity/mass deffect on the thermal conductivity.
To avoid the need of repeating the calculation of the thermal conductivity, it has been included the option `I_SF` (Impurity Scaling Factor).

