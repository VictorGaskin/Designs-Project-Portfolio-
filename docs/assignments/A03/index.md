# A3 – [Topic]

## Objective
The purpose of this assignment was to utillize design parameters to create a beam that would not surpass a given threshold, and use Finite Element Analysis to verify the validity of previous results. 


## Analyze
The parameters of the project had a few strict requirments to choose. 
Firstly, the bar cross section needed to be circular, secondly the force applied to the bar had to be between 300 lb/f and 500lb/f, the maximum axial deflection of the bar was .009 inches, and lastly the material used for the bar had to be aluminum with a Young's Modulus between (8.5-11.5)* 10^6 pounds per square inch. 

### Given

The initial parameters for my chosen bar is below: 
Material: 6061-T6 Aluminum 
Applied Load: 300lb/f
Young's Modulus(E): 10.0 * 10^6 psi 
Diameter of bar = 2.0 inches

#### Minimum Length in order to satisfy maximum deflection. 

Calculations are listed below. 
Note: Solidworks listed the modulus of elasticity for 6061-T6 Aluminium as 10,007,004 psi, but most sources I found listed 10,000,000 psi(68.9GPa) 

Source: https://www.gabrian.com/wp-content/uploads/2018/09/6061-Aluminum-Alloy-Properties-1.pdf

<img width="1163" height="1280" alt="image" src="https://github.com/user-attachments/assets/5ef8df09-4f90-4453-adad-eafc5b7596b6" />

I intially thought that my length calculated was absurd and verified my calculations. I eventually realized that .009 inches is about a grain of sand's worth of bending in the beam. Since the maximum distance needed is so absurdly small, it was logical. Through my verification, I discovered that the common accepted maximum deflection is L/360, so in a 20 foot beam .67 inches of deflection is allowed. The minimum deflection for this project is 74 times smaller than this. 

#### Solidworks Modeling

I started my design by creating all global variables used in the design equations used to calculate the minimum length in design equation. 

<img width="1362" height="567" alt="image" src="https://github.com/user-attachments/assets/0dd69d3e-4ff3-4fe5-ae44-11ca1677c408" />


Next I created a sketch with the exact diameter that was chosen in the intital parameters, I attached a driven global dimension "dia" to that value. I then extruded the sketch to length "L", which was also a global variable to create my bar. 

<img width="2048" height="1247" alt="image" src="https://github.com/user-attachments/assets/cb6ae0b5-0909-4a21-8a17-614f4a9dcc3c" />

Next, I assigned my material to the beam to prepare it for FEA. I chose 6061-T6 Aluminum.

The 6061-T6 Aluminum had a Young's Modulus that was 7,004 psi higher. This effects the calculations by a couple thousandths. 

#### Global Variable Verification

To verify that my bar length was interacting properly with the parametric global variables, I modified the intitial force to be 450 lb/ft to determine behavior. 

<img width="1332" height="465" alt="image" src="https://github.com/user-attachments/assets/bbb69ab7-2ff9-48c7-a2b3-f7f02b0dfccb" />

The model changed as expected, the length of the beam reduced to around 630 inches(compared to the approximately 800 inches before variable change) 

<img width="2048" height="1187" alt="image" src="https://github.com/user-attachments/assets/9d98d1cb-dda0-4f47-9b85-6a8485cee26c" />



#### Finite Element Analysis

With the global variable behavior verified, I could continue to FEA analyis. 

In my bar, I made the left end of the bar my fixed geometry and the right end where my force would act upon. I ran a deflection test and Van Miseser Test 

1. Deflection Curve:
   Running the simulation for deflection, I found that the point where deflection was highest was the tip of the bar where the force made first contact. The chart was in mm so I had to convert to inches.

   Maximum deflection in bar was found to be 2.29 x 10^-1 mm, which is .009 in^2.
   <img width="1536" height="1307" alt="image" src="https://github.com/user-attachments/assets/e17dc34d-c53b-4984-a4ef-b57021920bd1" />

2. Von Mises Stress Curve
  Running the Von Mises Stress simulation found that the stress was evenly distributed throughout the entire length of the bar. The orange color was assigned to 7.624 x 10^5 N/m^2. Converting to lbs/in^2 I found the maximum stress w as 110.57 psi.

<img width="1536" height="1283" alt="image" src="https://github.com/user-attachments/assets/ebedb5fd-70c2-4d39-8cfa-3b82298fa2bb" />

The yield strenth of aluminum was identified to by 40ksi(40,000 psi), dividing this value by maximum stress of the bar delivers a safety factor of about 361. 

Solidworks's analysis yielded a similar result. 
<img width="795" height="197" alt="image" src="https://github.com/user-attachments/assets/0af91ad3-94ad-4985-9478-8d1237df366a" />

   
### Results

The maximum axial deflection in the beam according to the FEA software was .009 inches, this is exactly the same as my hand calculations, which verifies this solution. 

Out of curiosity I wanted to determine how close the normal stress would be to my hand calculations. I calculated the stress on the beam using my given values. 

<img width="3072" height="529" alt="image" src="https://github.com/user-attachments/assets/fef4ca24-c77b-4576-995e-d4abfa9d3ded" />

Since these two values are essentially the same, I would most likely choose the CAD software calculation, since this software is used in industry, it may be configured with more nuanced material properties. However, if I had an official manifest that mentioned the exact value for Young's modulus used in manufacturing, I would trust the calculations done by hand. 


b. For the hypothetical hole placed within the beam, I found that Kt factor is about a range of 2.0 to 3.0. Assuming the highest amount of 3.0, that would raise the concentration of stress to 330 psi. This value would pass the FEA, as the yield strength is still 40ksi. The stress concentration that the hole creates is only 0.825% of the maximum yield strength. The beam would be unaffected due to the change in stress due to the stress concentration being almost negligible. 


## Decide


## Communicate

results
