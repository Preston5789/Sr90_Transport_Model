# MODELING STRONTIUM-90 TRANSPORT AND POTENTIAL REMEDIATION FROM A CONTAMINATED AQUIFER

## Abstract
<p align="center">
  <img src="https://github.com/Preston5789/Sr90_Transport_Model/blob/master/ThesisPics/Underground.PNG" width="400" title="hover text">
</p>

Radioactive waste injected into depleted oil reservoirs runs the risk of contaminating local aquifers if the bore casing of the injection hole were to fail. The currently proposed method of remediation involves multiple iterations of flushing to remove all contaminants. This is inefficient as the radionuclides adsorb into the aquifer rock and desorb back into the water table after a period of time. The adsorption/desorption kinetics for the activity concentration in the injection solution have been transformed into first order rate equations to model the interactions over time. The adsorption of Sr-90 has been modeled as a competitive process between two categories of rock.
In parallel, almond hulls have been proposed as potential biosorbents for Sr-90. The kinetics have also been modeled into first order equations. This study quantifies how the addition of the almond hull kinetics will affect the activity concentration in the injection solution and within the two rock types. It simulates how the addition of an almond hull biosorbent into the injection solution would immobilize the radionuclides reducing the activity in the surrounding rock. With the biosorbent added to the system, the activity concentration in the injection solution is 39% of the activity concentration without by the 10th day. It was found that there was an 62% reduction in the total activity concentration in Rock Type 1 and Rock Type 2 after 10 days compared to adsorption using no biosorbent.

## The Math

### Combining Models

The purpose of this thesis is to integrate a biosorbent model into the dual-site-one-component model of the rock. The almond hull is treated as a third compartment that will compete for the adsorption of Sr-90. Both the almond hull model and the dual-site one component model are defined by first order rate equations discussed in the literature review. Both of the rate equations for the fluid activity concentration are combined and modeled using Euler’s Method as described in the following sections.

The two rate equations for each rock type (Equations 5 and 6) need to be expressed as one rate equation for the injection solution 𝑑𝐶/𝑑𝑡. The derivative of Rumynin’s Mass Balance Equation (Equation 9) can be taken to solve for the 𝑑𝐶/𝑑𝑡 term needed to solve for the system of differential equations. The method used to solve the differential equations is discussed further in Section 3.3. The first derivative of Rumynin’s Mass Balance is taken to get:

### Numerical Solving

The composite model was numerically solved using Euler's method. Euler’s method is used to approximate solutions to first order differential equations. We are using this as a numerical integration technique for estimating the solutions to this system of differential equations. As an example, suppose that we are given the following:

<img src="/tex/24026b05206d753c30bfcc87169de526.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=85.76581365pt height=30.648287999999997pt/>
<img src="/tex/98f8a4cba039c499e26ca1d534db3883.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=72.77935169999999pt height=24.65753399999998pt/>

Where f(x, y) is a known function and yo is a known initial value. We want to solve for y(x). Therefore, the point (xo, yo) is an exact value known to lie on the solution curve. Then, at some arbitrary value of x:

<img src="/tex/27f1e829498ef9c7400c40622d18e87f.svg?invert_in_darkmode&sanitize=true&sanitize=true" align=middle width=186.98920184999997pt height=24.65753399999998pt/>

If the difference between x=x1 and xo is small enough, then the point y=y1 on the tangent line should be a close approximation of the actual value of the solution y(x1). Therefore:

<img src="/tex/bdc73016433289b3ce41894da15dd6aa.svg?invert_in_darkmode&sanitize=true" align=middle width=201.14834684999997pt height=24.65753399999998pt/>

To solve for y1, the same principal can be applied. 

<img src="/tex/80148b0b76b7bd58a874dcd42684f32c.svg?invert_in_darkmode&sanitize=true" align=middle width=201.40419254999998pt height=24.65753399999998pt/>

Where 𝑦1 and 𝑓(𝑥1,𝑦1) are already known quantities. Assuming that the difference between each consecutive x value is equal to h, then a recursive formula is produced:

<img src="/tex/65c6d2d3eb10680105084e51d017a8ce.svg?invert_in_darkmode&sanitize=true" align=middle width=104.8096995pt height=22.831056599999986pt/>

<img src="/tex/ec8ab53ed81a08142903a6f5a0642eab.svg?invert_in_darkmode&sanitize=true" align=middle width=182.92257719999998pt height=24.65753399999998pt/>

The smaller the value of h, the better the approximation of y.

## Link To Published Paper

https://mountainscholar.org/bitstream/handle/10217/197255/Phillips_colostate_0053N_15475.pdf?sequence=1&isAllowed=y
