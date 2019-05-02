# MODELING STRONTIUM-90 TRANSPORT AND POTENTIAL REMEDIATION FROM A CONTAMINATED AQUIFER

## Abstract
<p align="center">
  <img src="https://github.com/Preston5789/Sr90_Transport_Model/blob/master/ThesisPics/Underground.PNG" width="400" title="hover text">
</p>

Radioactive waste injected into depleted oil reservoirs runs the risk of contaminating local aquifers if the bore casing of the injection hole were to fail. The currently proposed method of remediation involves multiple iterations of flushing to remove all contaminants. This is inefficient as the radionuclides adsorb into the aquifer rock and desorb back into the water table after a period of time. The adsorption/desorption kinetics for the activity concentration in the injection solution have been transformed into first order rate equations to model the interactions over time. The adsorption of Sr-90 has been modeled as a competitive process between two categories of rock.
In parallel, almond hulls have been proposed as potential biosorbents for Sr-90. The kinetics have also been modeled into first order equations. This study quantifies how the addition of the almond hull kinetics will affect the activity concentration in the injection solution and within the two rock types. It simulates how the addition of an almond hull biosorbent into the injection solution would immobilize the radionuclides reducing the activity in the surrounding rock. With the biosorbent added to the system, the activity concentration in the injection solution is 39% of the activity concentration without by the 10th day. It was found that there was an 62% reduction in the total activity concentration in Rock Type 1 and Rock Type 2 after 10 days compared to adsorption using no biosorbent.

## The Math

The composite model was numerically solved using Euler's method. Euler’s method is used to approximate solutions to first order differential equations. We are using this as a numerical integration technique for estimating the solutions to this system of differential equations. As an example, suppose that we are given the following:

![\frac{dy}{dt}=f(x,y)](https://latex.codecogs.com/svg.latex?x%3D%5Cfrac%7B-b%5Cpm%5Csqrt%7Bb%5E2-4ac%7D%7D%7B2a%7D)
![y(x_o)-y_o](https://latex.codecogs.com/svg.latex?x%3D%5Cfrac%7B-b%5Cpm%5Csqrt%7Bb%5E2-4ac%7D%7D%7B2a%7D)

Where f(x, y) is a known function and yo is a known initial value. We want to solve for y(x). Therefore, the point (xo, yo) is an exact value known to lie on the solution curve. Then, at some arbitrary value of x:

![y=y_o + f(x_o,y_o)(x-x_o)](https://latex.codecogs.com/svg.latex?x%3D%5Cfrac%7B-b%5Cpm%5Csqrt%7Bb%5E2-4ac%7D%7D%7B2a%7D)
