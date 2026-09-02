# A2 – Truss Stress Analysis

## Objective
The objective of this project is to assemble a truss system, analyze the internal forces within it, and model it parametrically to verify results. 


## Analyze


## Decide

_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

I selected a design that had the minimum amount of members required to provide stability given the loads applied. I chose a triangular design for the truss due to triangles being inherently rigid and more material efficient compared to similar rectangular truss designs. I considered a design where a beam would have subtended the inside of the center triangle. However I opted out of this decision because there was no forces applying a load on the top of the truss, where such a beam would have benefitted the truss the most. Avoiding zero force members was the goal, as a beam that is not aiding in supporting the overall load is extremely wasteful.

<embed image here> 

## Communicate

The first step in the design process was to solve the truss for all of the external forces. This was simple due to forces P and pins C and D. 
<embed FDB>

The choice for a simpler truss design aided in the analysis of internal forces. The truss had 7 individual members and 6 pins(including an added pin E, which in subsequent calculations is rendered negligible). 5 pins had to be solved in order to have thoroughly analyzed. I chose to solve for Pins A, B, C, and D due to those pins being listed points in the problem statement. 

At first I chose to use the method of sections to analyze the internal forces of the truss, in order to cut down on the time spent solving. After some deliberation, I opted to utilize the method of pins because it would allow me to have a greater understanding of what exactly was happening within the truss. I made this decision with the knowledge that it would greatly extend the time spent solving

### Major Difficulties

Difficulties arose in solving due to the truss design I chose. Due to the center of the truss having a different length than the ones surrounding it, solving for the inner angles of this triangle became a laborious task, as such angles were necessary for finding force members. This is most apparent for Pins C and D of which are points of this triangle. 

Representing the internal forces of the truss symbolically was a roadblock due to confusion of how to represent trigonometric functions without using the arguments of sin/cos as well as their corresponding angles. Eventually I realized that these arguments can be represented as the ratio of lengths between the triangles, although this now required me to remember which argument I would be referring to when I solved the truss numerically. This roadblock slowed down the solving of the truss by 2 hours, as various steps needed to be double checked and verified against the numerical answers in order to be logically consistent. 

Eventually, I completed both the symbolic and numerical verification of the internal forces of the truss. Ensuring consistency between both. This did require me to redo the calculations of the truss to provide space for more legible documentation

<embed final image for both> 

Next, I had to calculate the minimum cross sectional area for the rods of the truss to support the greatest normal stress, the weight of the truss given the found cross sectional area, as well as the minimum cross sectional area of the pins to support the greatest shear stress. Both calculations for the rods and pins had safety factor considerations of 3.5 and 4 respectively. 

### Minimum Cross Sectional Area Calculation

Before solving for the minimum cross sectional area of any given beam in the truss, I had to consider the material being used. The initial parameters that the project was given listed A500 Steel, however upon further research(which was done to find the normal yield strength) I found that there is a multitude of A500 steel types used in industry. I settled on using Grade C A500 Steel as it is the most used steel for trusses. Due to making this assumption for the Grade of A500 steel being utilized, I averaged the range of yield strength(σᵧ) in order to ensure safety. This safety consideration was inserted because some steel may arrive over or under preforming their intended values. 

Solving for the minimum cross-sectional area required me to use the highest internal force from the previous calculation. In order to solve, I utilized a equality between the maximum normal stress present in the truss and the maximum allowable normal stress. Setting both equations equal to each other allowed for the minimum cross sectional area to be found. 

A significant error in my calculation was that I forgot to utilize proper dimensional analysis when calculating my units. In the image attached below I forgot to convert my maximum force into newtons in order to achieve the units of mm^2, which gave an cross sectional area 6.8 times larger than intended.
<embed error image> 
Note: (1,400.00 mm^2 vs 203.08mm^2)

After correcting for the minimum area required I took the square root of the result in order to get the length and width of the required cross section. This was because the cross sections of the truss were assumed to be square and thus needed a (# x #) format in order to achieve the desired area. A design choice that I made was to round the minimum cross sectional area up to the nearest whole number regardless of the decimal place. This was done to simplify the future modeling process. I am not unaware that this would raise manufacturing cost and weight, however the added safety and simplicity in design weighed heavier*. This decision raised the cross sectional area from 203.08mm^2 to 225mm^2 (in imperial units this is .3148in^2 to .3488 in^2) an 11% increase

<embed substitution expression>
### Truss Weight Calculation 

In order to calculate the weight of the truss I first found the combined length of every beam in the truss in meters. Using this value I calculated the volume of the beam in mm^3. I then realized since density of metals are usually given in kg/m^3, I had to use dimensional analysis to convert my volume in mm^3 into m^3. Next, I found the density(ρ) of A500 Grade C Steel online set up the equation for density. Mass was the unknown in this equation and was solved for. I converted my mass into empirical units for simplicity between audiences. 

<embed calculation of mass for truss> 


### Pin Calculation. 





