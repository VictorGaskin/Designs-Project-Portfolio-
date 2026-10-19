# A7 – Bracket Finite Element Analysis

## Objective
The Objective for this assignment was to analyze the bracket from assignments 5 and 6 and run a finite element analysis method in order to optimize bracket design.

## Analyze
The intial goals that are intended to be met or exceeded through this analysis goes as follows:

*Goals:
Factor of Safety > 4
Max Deflection <= 0.005in
Increase Strength to Weight ratio
Increase Stiffness to Weight ratio*

### Round 1: 
The purpose of Round 1 was to determine the starting conditions for the bracket, and whether which parameters would achieve convergence given only a change in mesh size. 

Medium Mesh Test: 

The results from the medium mesh test goes as follows: 

Lowest Factor of Safety(FOS): 252.42
Maximum Deflection: 8.472 x 10^-4 mm or 3.33 x 10^-5 inches 
  - Location at end of feature A where force is applied
Maximum Stress: 3.27 MPa
    - Location at corners of Model where Feature B attaches to frame
Mass: 0.07lbs

Fine Mesh Test: 
Lowest FOS: 197.808
Maximum Deflection: 8.767 x 10^4 mm
Maximum Stress: 4.18 MPa
Mass = 0.07 lbs 

### Convergence Check: 
I inputted all convergence values using this equation. 
  *C(a,b)=(2\operatorname{abs}(b-a)/(a+b))*100*
b represents X final. a represents x initial.  

Convergence Results for Round 1: 

Convergence of Deflections: 0.376%
Convergence of Stresses = **21.75%**
Convergence of FOS = *22.22%*

*Note: These values did not deviate by greater than 0.1% with repeated testing.* 

Results: 
Deflections converged nicely, but stresses did not. The goal for further rounds of FEA is to optimize the stresses to get as close to converging as possible. 
  The Factors of Safety not converging is less important due to both values being vastly above our desired safety factor of 4, but convergence of FOS is intended as well. 
  
### FEA Mesh Comparison
| Parameter | FEA 1 (Coarse) | FEA 2 (Fine) |
|:--|:--:|:--:|
| Max Stress (psi) |  |  |
| Stress Location | <img width="350" alt="Coarse Mesh Stress" src="" /> | <img width="350" alt="Fine Mesh Stress" src="" /> |
| Max Deflection (in) |  |  |
| Deflection Location | <img width="350" alt="Coarse Mesh Displacement" src="" /> | <img width="350" alt="Fine Mesh Displacement" src="" /> |
| Mass (lb) |  |  |
| Minimum Safety Factor |  |  |
| Safety Factor Location | <img width="350" alt="Coarse Mesh Safety Factor" src="" /> | <img width="350" alt="Fine Mesh Safety Factor" src="" /> |
| Number of Mesh Elements |  |  |

### Round 2: 
The purpose of Round 2 was to achieve convergence in the stress values, as well to reduce the stress concentrations happening within the model. 

Pre-Test: Symmetric Filets with a radius of 0.05in were added at the corners of feature B as well as the rounded edge of feature A. 

<img width="2515" height="1437" alt="Pre Round 2 Fillet Addition" src="https://github.com/user-attachments/assets/ca94a05f-2396-44d8-a8d7-cf87657b3bea" />
<img width="2527" height="1400" alt="Pre Round 2 Chamfer Addition" src="https://github.com/user-attachments/assets/f6ff1003-dfd0-4892-8c27-e5c912d94377" />


Medium Mesh Test: 

The results from the medium mesh test goes as follows: 

Lowest Factor of Safety(FOS): 215.098
Maximum Deflection: 8.544 x 10^-4 mm or 3.36 x 10^-5 inches 
  - Location at end of feature A where force is applied
Maximum Stress: 3.84 MPa
    - Location at corners of Model where Feature B attaches to frame
Mass: 0.07lbs

Fine Mesh Test: 
Lowest FOS: 200.757
Maximum Deflection: 8.529 x 10^4 mm
Maximum Stress: 4.22 MPa
Mass = 0.07 lbs 

Convergence Results for Round 1: 

Convergence of Deflections: 0.293%
Convergence of Stresses = **7.059%**
Convergence of FOS = *6.897%*

*Note: These values did not deviate by greater than 0.1% with repeated testing.* 

Adding the chamfers into the design significantly decreased the variation within both the stresses and safety factors within the model. 

### Round 3: 
The purpose of Round 3 was to further tune the convergence in the stress values, as well as increasing the strength-to-weight, stiffness-to-weight, and location of stress concentrations. 

Pre-Test: At first I removed a considerable amount of material from the center of my bracket. The hope was for this to preserve the integrity of the model while reducing weight. This caused a catastrophic change in my models integrity, dropping the smallest factor of safety to 19. 

I scrapped this proposed change and instead added 20 degree filets to the corners where stress concentrations where occurring previously.  

<img width="2460" height="1400" alt="Round 3 Material Removal" src="https://github.com/user-attachments/assets/6c66e444-3d7f-4f7b-8cd6-19fe2acadb71" />
<img width="2460" height="1430" alt="Round 3 Cut " src="https://github.com/user-attachments/assets/1446e843-07ff-4761-a9b0-96a66a03b30b" />



Medium Mesh Test: 
Lowest FOS: 211.532
Maximum Deflection: 8.317 x 10^4 mm
  - Location at End of Feature A
Maximum Stress: 3.91 MPa
  - Location at Backside of Filet
Mass = 0.07 lbs

Fine Mesh Test: 

The results from the medium mesh test goes as follows: 

Lowest Factor of Safety(FOS): 193.258
Maximum Deflection: 8.449 x 10^-4 mm or 3.36 x 10^-5 inches 
  - Location at end of feature A where force is applied
Maximum Stress: 3.84 MPa
     - Location at Backside of Filet
Mass: 0.07lbs

Convergence Results for Round 1: 

Convergence of Deflections: 0.157%
Convergence of Stresses = **1.08%**
Convergence of FOS = *9.03%*

Significantly more accuracy between deflection and stress convergence when filets were added. Alongside this, the strength/weight ratio was increased with stiffness/weight as model weight did not increase by more than 0.001 lbs while yielding better results. 

*Note: These values did not deviate by greater than 0.1% with repeated testing.* 



## Decide


## Communicate

