# A2 – Truss Stress Analysis

## Objective
The objective of this project is to assemble a truss system, analyze the internal forces within it, and model it parametrically to verify results. 


## Analyze


## Decide

_Which geometry did you select, and why? This is your first open design choice in the course — defend it._

I selected a design that had the minimum amount of members required to provide stability given the loads applied. I chose a triangular design for the truss due to triangles being inherently rigid and more material efficient compared to similar rectangular truss designs. I considered a design where a beam would have subtended the inside of the center triangle. However I opted out of this decision because there was no forces applying a load on the top of the truss, where such a beam would have benefitted the truss the most. Avoiding zero force members was the goal, as a beam that is not aiding in supporting the overall load is extremely wasteful.

<img width="2048" height="1267" alt="image" src="https://github.com/user-attachments/assets/2c708b45-4415-485d-a47b-c80e59ef84b7" />


## Communicate

The first step in the design process was to solve the truss for all of the external forces. This was simple due to forces P and pins C and D. 
<img width="1127" height="1280" alt="image" src="https://github.com/user-attachments/assets/9fc851ba-b1ec-4517-b041-649bbd3d7254" />


The choice for a simpler truss design aided in the analysis of internal forces. The truss had 7 individual members and 5 pins(including an added pin E, which in subsequent calculations is rendered negligible). 4 pins had to be solved in order to have thoroughly analyzed. I chose to solve for Pins A, B, C, and D due to those pins being listed points in the problem statement. 

At first I chose to use the method of sections to analyze the internal forces of the truss, in order to cut down on the time spent solving. After some deliberation, I opted to utilize the method of pins because it would allow me to have a greater understanding of what exactly was happening within the truss. I made this decision with the knowledge that it would greatly extend the time spent solving

### Major Difficulties

Difficulties arose in solving due to the truss design I chose. Due to the center of the truss having a different length than the ones surrounding it, solving for the inner angles of this triangle became a laborious task, as such angles were necessary for finding force members. This is most apparent for Pins C and D of which are points of this triangle. 

Representing the internal forces of the truss symbolically was a roadblock due to confusion of how to represent trigonometric functions without using the arguments of sin/cos as well as their corresponding angles. Eventually I realized that these arguments can be represented as the ratio of lengths between the triangles, although this now required me to remember which argument I would be referring to when I solved the truss numerically. This roadblock slowed down the solving of the truss by 2 hours, as various steps needed to be double checked and verified against the numerical answers in order to be logically consistent. 

Eventually, I completed both the symbolic and numerical verification of the internal forces of the truss. Ensuring consistency between both. This did require me to redo the calculations of the truss to provide space for more legible documentation

<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/b2aa2ee0-2a79-44b9-9aac-564a08b0ca2a" />

<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/8c57b704-2086-4081-a10d-92d092494fc3" />

Next, I had to calculate the minimum cross sectional area for the rods of the truss to support the greatest normal stress, the weight of the truss given the found cross sectional area, as well as the minimum cross sectional area of the pins to support the greatest shear stress. Both calculations for the rods and pins had safety factor considerations of 3.5 and 4 respectively. 

### Minimum Cross Sectional Area Calculation

Before solving for the minimum cross sectional area of any given beam in the truss, I had to consider the material being used. The initial parameters that the project was given listed A500 Steel, however upon further research(which was done to find the normal yield strength) I found that there is a multitude of A500 steel types used in industry. I settled on using Grade C A500 Steel as it is the most used steel for trusses. Due to making this assumption for the Grade of A500 steel being utilized, I averaged the range of yield strength(σᵧ) in order to ensure safety. This safety consideration was inserted because some steel may arrive over or under preforming their intended values. 

Solving for the minimum cross-sectional area required me to use the highest internal force from the previous calculation. In order to solve, I utilized a equality between the maximum normal stress present in the truss and the maximum allowable normal stress. Setting both equations equal to each other allowed for the minimum cross sectional area to be found. 

<img width="1077" height="614" alt="image" src="https://github.com/user-attachments/assets/934d203e-78ad-4f09-8c16-effaed34fd25" />

### Major Error
A significant error in my calculation was that I forgot to utilize proper dimensional analysis when calculating my units. In the image attached below I forgot to convert my maximum force into newtons in order to achieve the units of mm^2 as well as not converting my stress in ksi in terms of psi, which gave an cross sectional area 6.8 times larger than intended.

Note: (1,400.00 mm^2 vs 203.08mm^2)
<img width="2491" height="2160" alt="image" src="https://github.com/user-attachments/assets/4ee0d8bf-f996-44db-a7e6-61005ffe3827" />


After correcting for the minimum area required I took the square root of the result in order to get the length and width of the required cross section. This was because the cross sections of the truss were assumed to be square and thus needed a (# x #) format in order to achieve the desired area. A design choice that I made was to round the minimum cross sectional area up to the nearest whole number regardless of the decimal place. This was done to simplify the future modeling process. I am not unaware that this would raise manufacturing cost and weight, however the added safety and simplicity in design weighed heavier*. This decision raised the cross sectional area from 203.08mm^2 to 225mm^2 (in imperial units this is .3148in^2 to .3488 in^2) an 11% increase

<img width="3072" height="1353" alt="image" src="https://github.com/user-attachments/assets/b986f4de-ba5c-4d82-82c9-9a2f85c4117f" />

### Truss Weight Calculation 

In order to calculate the weight of the truss I first found the combined length of every beam in the truss in meters. Using this value I calculated the volume of the beam in mm^3. I then realized since density of metals are usually given in kg/m^3, I had to use dimensional analysis to convert my volume in mm^3 into m^3. Next, I found the density(ρ) of Grade C A500 Steel online set up the equation for density. Mass was the unknown in this equation and was solved for. I converted my mass into imperial units for simplicity between audiences. 

Image below portrays the final mass calculation with all errors omitted:

<img width="940" height="1280" alt="image" src="https://github.com/user-attachments/assets/f9ed174f-d859-42e9-8e1e-536903702cd2" />



### Pin Calculation. 

#### Pins: Cross Sectional Area

As I went to calculate the cross sectional area for the pins, a few considerations had to be understood. The pins were assumed to be able to withstand buckling, which mean that the forces that would cause buckling were not considered with this calculation. The factor of safety for the pins were slightly higher than for the body of the truss, being 4 instead of 3.5 respectively. The material used for the pins were different than the body of the truss, and lastly that the pin connections were designed for single shear. 

Firstly a free body diagram was developed to model the direction of shear. Once that was determined a similar equation to the one used to determine the cross sectional area for the truss body was utilized, substituting normal stress for shear stress. The method for solving for variable Across was identical to the minimum cross sectional area for the beam.  

##### Minor Errors 

Initial errors in my calculations came from forgoing unit conversions between ksi and psi. This error was caught quickly and does not occur again for the remainder of this project

##### Results

The final calculation for the cross sectional area of the pins is below: 

<img width="1052" height="1280" alt="image" src="https://github.com/user-attachments/assets/dfbd7d17-7ce2-48ea-8a8f-c2f8a16db2bd" />

#### Pins: Weight

A few considerations I had to keep in mind before starting the weight calculation of the pins was that the specific type of hardened tool steel was not described. I could have used a general range of tool steel densities in order to calculate, but I opted to know exactly what type of steel I would use in order to ease replicability and increase consistency. I chose H13 Tool Steel as it had the lowest weight per in^3 of other tool steels that were listed

##### Mistakes

A mistake that was made through the volume calculation was that I mistook my first answer for mass to be in units of lbs instead of lbs per inches. This error occured because I did not consider the thickness of the pins had to at minimum be as thick as the cross sections of the truss beams. 

I also forgot to calculate the radius of the pins when I had calculated the cross sectional area. If the radius was calculated from this step, it would have eased the modeling process in SOLIDWORKS.

An image of this error: 

<img width="1536" height="1043" alt="image" src="https://github.com/user-attachments/assets/9c630653-a7bd-4a5f-9898-185c25c6ea17" />

##### Results

With a better understanding for the pin calculations, I opted to add an extra 0.5mm of length to the pins. This was because truss pins are not made to be press fit, instead they are designed in order to be replaced whenever necessary. 

Knowing the intended length for the pins, the volume of the pins could be calculated, and the weight could be found with the given/obtained values. Since my truss was designed with five pins, I multiplied the found pin weight by 5 to account for those extra pins.

The complete calculations: 
<img width="2160" height="2999" alt="image" src="https://github.com/user-attachments/assets/21ec98b8-d60a-435a-a4c0-ebb3418c0b0b" />


### Truss Modeling 

The computer aided modeling software used for this portion of the project was SOLIDWORKS 

SOLIDWORKS FILE: 



#### Method 

The model of the truss system was designed as a single rigid body instead of an assembly per the project instructions. 




SOLIDWORKS does not natively support the material used for the truss(A500 Steel), instead of recalculating the properties of the truss with another material. I instead created a custom material within the software and imported the material properties of Grade C A500 steel manually.
<img width="2035" height="1690" alt="image" src="https://github.com/user-attachments/assets/4f4fdd68-38ec-4b2f-82f0-06cb9dfd2f1f" />

Material Properties Utilized
<img width="1142" height="540" alt="image" src="https://github.com/user-attachments/assets/04adcffc-542a-40e4-ad51-c71c3bb74fa9" />

These steps ensured the subsequent weight of the truss would be as accurate as possible. 


#### Modeling 

I used the line tool to create the "skeleton" of the truss, ensuring that the exact length ratios used in the truss calculations were preserved. Thankfully, SOLIDWORKS automatically converts metric measurements into English units.

<img width="1000" height="775" alt="image" src="https://github.com/user-attachments/assets/c526f973-9948-44bc-9d08-29f8ca98a182" />


Afterwards, I used a built in tool(Structural Member) used to model beams in place of extruding the entire piece. I ensured that the cross sections would still be square to ensure consistency with previous calculations. This also includes where the pins would be.

<img width="2880" height="1752" alt="image" src="https://github.com/user-attachments/assets/3e782fc2-3224-40ff-8192-1d2942c4d8de" />


Lastly, I could use the mass properties analysis tool to find the weight of the model truss. 
<img width="1075" height="455" alt="image" src="https://github.com/user-attachments/assets/4bad566c-00e5-4a37-b364-bae43429cce3" />


##### Comparison

The difference in weight between the CAD model and my calculations were about 13 percent. The previously calculated weight was 12.97 lbs compared to the models 14.96 lbs 



### Engineering Lessons Learned 

The major lessons learned within this assignment was that is extremely important to keep track of units, especially when completing dimensional analysis. There was a multitude of times throughout the project where the conversions between metric and English units, or similar units of pressure or volume caused cascading errors within the project that took upwards of an hour to rectify. This demonstrated how important it was to have symbolic representations of the problems before I plugged in any values. 

Alongside this, this project demonstrated the stark difference between how engineering design can change between the conception and execution phases. I learned how to narrow down and specify where the design needed to be adapted in order to fit within the parameters given. This included the specification of the material type, sizes of specific part to work within real engineering, and CAD modeling to ensure accuracy to the previously mentioned parameters. 

In addition to the challenges, I learned value information about the use cases and material properties of Grade C A500 Steel and H13 Tool Grade Steel.

Overall, this project taught me how to carefully manage units and dimensional analysis, use symbolic equations to prevent calculation errors, adapt an engineering design to meet specific constraints, and apply material properties when selecting appropriate materials. It also helped me understand the differences between the initial design concept and the final engineered design through sizing, material selection, and CAD modeling.


### Truss Members Failure Analysis

#### 1. Members whose most likely failure mode is Yielding

The members whose failure mode would be yielding is BC, BE, CE, DE, 

CE and DE would be the most likely members to fail due to yielding because of both members having the highest internal loads placed on them due to the external forces P on their pin joints. 

#### Members whose most likely failure mode is Buckling 

Since buckling is indicative of members that are in compression, only member AD would be able to buckle significantly.

#### Exceptions 

CD is a zero force member, so it is the absolutely least likely member to fail. 


#### 2. Material Quality
The materials that make up the members of the truss are ductile

#### 3. Justification

*Source: https://baling-steel.com/astm-a500-grade-b-properties/*
Due to each member being made of A500 Steel, each member would be ductile. This makes sense due to truss needed to show warning signs before failure to preserve human lives. Furthermore, lower carbon steels are more ductile than their lower carbon counterparts. Grade C A500 steel has a carbon content of 0.23% compared to the ~0.60% range of high carbon steels. 

#### 4. Preventative Measures 

A preventative measure that could be taken to prevent the most prevalent failure mode in this truss(yielding) is slightly lengthen the members by a smaller safety factor in order to better distribute the forces throughout the beam. 


### Pin Failure Analysis

#### 1. Expected Failure Modes 

Akin to the rest of the truss members, most of the pins are undergoing tension. This would lead the pins to most likely undergo pin bending. 

#### 2. Justification 

*Source: https://www.sciencedirect.com/science/article/pii/S0143974X22006228*

The pins would have the forces from the rest of the internal beam and external forces shifted onto them. The Journal of Constructional Steel Research confirmed the behavior of pins when undergoing a bending moment due to shear. This proves that this is a considerable failure mode in pins under yield. 

#### 3. Design Modifications 

A design modification that could significantly reduce the chance of pins failing due to pin bending is increasing the diameter of the pin. Increasing the width of the pins will allow them to withstand more forces before starting to fail.



