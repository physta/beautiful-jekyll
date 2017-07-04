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

<center> <b>q</b> = -&lambda;<b>&nabla;</b>T+&ell;<sup>2</sup> </center>

<math display='block'> 
  <mfrac> <mrow> &part;&tau; 
        <mrow>
          &part;t
        </mrow>
      </mfrac>
  </mrow>
</math>
