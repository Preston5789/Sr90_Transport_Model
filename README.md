# MODELING STRONTIUM-90 TRANSPORT AND POTENTIAL REMEDIATION FROM A CONTAMINATED AQUIFER

## Abstract
<p align="center">
  <img src="https://github.com/Preston5789/Sr90_Transport_Model/blob/master/ThesisPics/Underground.PNG" width="400" title="hover text">
</p>

Radioactive waste injected into depleted oil reservoirs runs the risk of contaminating local aquifers if the bore casing of the injection hole were to fail. The currently proposed method of remediation involves multiple iterations of flushing to remove all contaminants. This is inefficient as the radionuclides adsorb into the aquifer rock and desorb back into the water table after a period of time. The adsorption/desorption kinetics for the activity concentration in the injection solution have been transformed into first order rate equations to model the interactions over time. The adsorption of Sr-90 has been modeled as a competitive process between two categories of rock.
In parallel, almond hulls have been proposed as potential biosorbents for Sr-90. The kinetics have also been modeled into first order equations. This study quantifies how the addition of the almond hull kinetics will affect the activity concentration in the injection solution and within the two rock types. It simulates how the addition of an almond hull biosorbent into the injection solution would immobilize the radionuclides reducing the activity in the surrounding rock. With the biosorbent added to the system, the activity concentration in the injection solution is 39% of the activity concentration without by the 10th day. It was found that there was an 62% reduction in the total activity concentration in Rock Type 1 and Rock Type 2 after 10 days compared to adsorption using no biosorbent.

## The Math

The composite model was numerically solved using Euler's method. Euler’s method is used to approximate solutions to first order differential equations. We are using this as a numerical integration technique for estimating the solutions to this system of differential equations. As an example, suppose that we are given the following:

<img src="/tex/24026b05206d753c30bfcc87169de526.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=85.76581365pt height=30.648287999999997pt/>
<img src="/tex/98f8a4cba039c499e26ca1d534db3883.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=72.77935169999999pt height=24.65753399999998pt/>

Where f(x, y) is a known function and yo is a known initial value. We want to solve for y(x). Therefore, the point (xo, yo) is an exact value known to lie on the solution curve. Then, at some arbitrary value of x:

<img src="/tex/27f1e829498ef9c7400c40622d18e87f.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=186.98920184999997pt height=24.65753399999998pt/>

If the difference between x=x1 and xo is small enough, then the point y=y1 on the tangent line should be a close approximation of the actual value of the solution y(x1). Therefore:

<img src="/tex/1ea8e5ca49fc6b064fdf0dfc91295cf3.svg?invert_in_darkmode&sanitize=true" align=middle width=202.63231559999997pt height=24.65753399999998pt/>

To solve for y1, the same principal can be applied. 

<img src="/tex/80148b0b76b7bd58a874dcd42684f32c.svg?invert_in_darkmode&sanitize=true" align=middle width=201.40419254999998pt height=24.65753399999998pt/>

Where 𝑦1 and 𝑓(𝑥1,𝑦1) are already known quantities. Assuming that the difference between each consecutive x value is equal to h, then a recursive formula is produced:

<img src="/tex/65c6d2d3eb10680105084e51d017a8ce.svg?invert_in_darkmode&sanitize=true" align=middle width=104.8096995pt height=22.831056599999986pt/>

y_{n+1} = y_n + h*f(x_n,y_n)

The smaller the value of h, the better the approximation of y.
