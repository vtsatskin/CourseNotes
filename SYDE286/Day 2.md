# Mods
Normal Stress = $ \sigma = \frac P A $
Shear Stress = $ \tau = \frac V A $

* If $P > 0$: Tension, Tensile Normal Stress
* If $P < 0$: Compression, Compressive Normal Stress
* No such thing as a tensile or compressive shear stress

With every stress there is a corresponding distortion. To characterize the change in length due to a normal stress we use

$$\epsilon = \frac {\Delta L}{L} = \frac {\text{Change in Length}}{\text{Original Length}} = \text{Strain}$$

The relationship between $\sigma + \epsilon$ is determined experimentally.

## Stress and Strain Graph
Note: This discussion is for an iron alloy.

![Alt text](http://www.keytometals.com/img/screens/stress_strain_curve.gif)

* Starts at zero, zero stress and strain. Specimin is at original length.
* **Initial linear portion** will have a slope of $E$
  * This is called elastic of Young's modulus.
* **$A$ is proportional limit stress $\sigma_{PL}$**
  * End of the *linear elastic* region.
  * Beginning of the *non-linear* elastic region.
  * For $0 ≤ \sigma ≤ \sigma_{PL}, \sigma = E\epsilon$ (**Hooke's Law**)
  * As long as you don't pass $C$, there will not be any permanent deformation
* $C$ is the **Lower yield Point** $\sigma_{y}$
* $D$ is the **Upper Yield Point** 
* Between $D$ and $E$ there is a point in which the stress is constant (flat line), this is called the **plastic flow region**
  * Metal forming operates in this region.
* $E$ is the Maximum Stress
* $F$ is the Failure or Ultimate Stress (breaks.)

### Strain Hardening
![](http://qph.is.quoracdn.net/main-qimg-1ef12a6f115706a696191433099e6bca)

* Once you're past the elastic region (point $C$), the material will recover to a strain point denoted by the dotted line above.
* The slope of the line will have the same slope as the linear elastic portion, $E$
* Loading and unloading in the non-elastic region will follow the line from the point you start unloading, following the slope of $E$, until the stress is 0. Effectively creating a new linear-elastic region. This is called strain hardening.