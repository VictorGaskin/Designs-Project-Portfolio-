# A4 – [Topic]

## Objective

The objective of this project was to design a mount for a motor while balancing two different parameters, stress within a beam and deflection within the beam. 

Given Blueprints: 

<img width="1600" height="497" alt="image" src="https://github.com/user-attachments/assets/8a237363-8326-4b91-aa64-13ffe1f5cd4e" />

<img width="296" height="289" alt="image" src="https://github.com/user-attachments/assets/3d908eb7-e4e6-41d6-b4b9-a370a46f1cc9" />



## Analyze

### Design Decision: 

Before I could begin designing this project. I had to understand my givens as well as decisions that I would have to make. 

Firstly, the givens within the project parameters were as follows: 

Maximum Deflection(δ) = 0.30 mm 
Force(P) = 300 N 
Safety Factor = 3

Formula for deflection in a cantilevered beam
Formula for stress in a beam. 

The choice that I had to make was what material the base would be made out of and the base and length of the entire mount. 

I chose PETG to be the material for the mount due to it having the best durability for repetitive vibrational stress, which is what a motor would be applying on the frame constantly. 

This choice in material yielded a Yield Strength of 45 MPa and a Modulus of Elasticity of 2.1 GPa. 

I choose the base and length of the features of the mount to be 34mm for both, in order to keep my cross sections consistent throughout the modeling process.

#### Total List of Variables: 

Maximum Deflection(δ) = 0.30 mm 
Force(P) = 300 N 
Safety Factor = 3
base = length = 34mm 
Sy = 45MPa
E = 2.1 GPa

<img width="2048" height="1197" alt="image" src="https://github.com/user-attachments/assets/21f7c54c-9d61-44b8-aa5a-505d828df0f0" />


### Feature 1: 

I started solving for the height of feature one symbolically. Since this is the cantelevered end, there was a moment that needed to be considered due to the force P 18mm from the base. 

<img width="1280" height="1046" alt="image" src="https://github.com/user-attachments/assets/b14e151f-2bf3-40d3-b127-3c1950a7590c" />

After the expressions for H-Deflection and H-Stress were calculated. The given values could now be entered in order to calculate the height for feature one. 

Note: The larger of the h values was chosen, since we need to consider both the stress and deflection forces. 

<img width="2802" height="1320" alt="image" src="https://github.com/user-attachments/assets/649169c5-7b4f-4119-a228-5e790e2a098a" />


After the calculations, a height of 12.04 mm was chosen for feature 1. 

### Feature 2:

The only difference between the calculations between feature 1 and 2 is that I acertained that since feature 2 was mostly going to be mounted, that the distance that could possibly experience deflection is only 1/4 the given length. This was taken in account during the calculations, where variable L represents L/4. 

<img width="1536" height="989" alt="image" src="https://github.com/user-attachments/assets/9b7ce8c2-0f46-4fa5-901a-9405e7d2b0f9" />


After the calculations, a height of 5.47 mm was chosen for feature 2. 


### Sketch 

This is the rough sketch before the CAD model. Dimensions are listed on the sketch

<img width="1536" height="989" alt="image" src="https://github.com/user-attachments/assets/20a61377-74b2-4377-91da-5699e676ba76" />



### CAD MODEL 

Before I began to model the mount using my calculated dimensions, I inserted all the variables I used during calculations in order to ensure that my model would be parametric. 

Note: I only included the formulas for height that yielded that largest h value for each feature, since if you satisfy the parameter that requires the highest height you always will satisfy the other. 

<img width="995" height="440" alt="image" src="https://github.com/user-attachments/assets/573f6f27-8c19-4419-8200-4bf6ea41fcc7" />

Next, I proceeded to design the bodies of features one and two and extrude them, this was a bit of a struggle as I was still unfamiliar with the UI of SolidWorks. 

Note: The values are converted to inches by SolidWorks. The input dimensions were in mm.

<img width="690" height="670" alt="image" src="https://github.com/user-attachments/assets/f2d4375e-93ab-4a90-9c6b-236c9f30dafd" />

<img width="452" height="610" alt="image" src="https://github.com/user-attachments/assets/913c95f6-7fd1-4b08-8992-d49ea2061b74" />

With the general profile of the mount completed, I can now enter all the holes required to hold the body of the mount and the screws that would hold the rest of its profile. 

<img width="510" height="650" alt="image" src="https://github.com/user-attachments/assets/b73e1ecb-4fd4-42a0-bb75-aabc6b6882ad" />



This project also required a drawing to be attached to the project: 

https://github.com/VictorGaskin/Designs-Project-Portfolio-/blob/main/Motor%20Mount.SLDPRT










## Decide


## Communicate

