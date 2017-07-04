---
layout: page
title: Theoretical model 
description: Theoretical framework of the KCM 
---

### The Kinetic Collective Model

The Kinetic Colletive Model (KCM) developed in recent years improve the solution provided under the classical RTA.
The model, derived from the exact solution of the LBTE proposed by Guyer and Krumhansl,
is based on the splitting of the collision operator in normal and resistive processes (<b>C = N + R </b>) when calculating the scattering matrix.
As normal processes does not contribute directly to thermal resistance but redistribute momentum over all the phonon distribution,
a suitable way to solve the LBTE is by using the basis that diagonalizes the normal scattering collision operator.
This diagonalization allows to solve the BTE without complicating drastically the form of the drift operator.

The splitting of the collision operator allows to split the thermal conductivity in two contributions, kinetic and collective, 
weighed by a switching factor &Sigma; :

<center>&kappa; = (&Sigma; - 1)&kappa;<sub>kin</sub> + &Sigma;&kappa;<sub>col</sub>.</center>

![figkin](img/kinetic_regime.png) ![figcol](img/collective.png)

In the kinetic regime, each phonon behave independently, but in the collective regime, due to the effect
of <i>N</i> collisions apprears a coupling between phonons. Therefore phonons of different modes perform as a whole
resistive (R) collisions and share the same collision mean free time (MFT), the so-called collective MFT &tau;<sub>c</sub>.
 <br>
 <center><img class="ipsImage" src="https://physta.github.io/img/anim.gif" alt="img/anim.gif" width="400px" height="auto"></center>

For a full understanding of the KCM look at [References](https://physta.github.io/articles/).

### Hydrodynamic KCM 

As pointed out previously, using the basis that diagonalizes the normal scattering collision operator 
allows to study the drif operator in a simple way to higher orders, leading to:

<center> &part;&tau;/&part;t + <b>q</b>
 = -&lambda;<b>&nabla;</b>T+&ell;<sup>2</sup>(&nabla;<sup>2</sup><b>q</b>+2&nabla;&nabla;<b>q</b>), </center>

where <math>&ell;</math> is the non-local paramenter (NL-param). From [Guyer and Krumhansel](https://journals.aps.org/pr/abstract/10.1103/PhysRev.148.766){:target="_blank_"} it is studied
the limiting case where normal proceses dominate,  &tau;<sub>N</sub><<&tau;<sub>R</sub>. In this limit corresponding
to the collective regime, the NL-param is <math>&ell;<sup>2</sup><sub>N</sub>=&langle;v<sup>2</sup>&tau;<sub>N</sub>&rangle;&langle;&tau;<sub>C</sub>&rangle;</math>

<math>\sqrt[]{x}</math>

