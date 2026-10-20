# A7 – Bracket Finite Element Analysis

## Objective
The Objective for this assignment was to analyze the bracket from assignments 5 and 6 and run a finite element analysis method in order to optimize bracket design.

## Analyze
The intial goals that are intended to be met or exceeded through this analysis goes as follows:

Goals:
- Factor of Safety > 4
- Max Deflection <= 0.005in
- Increase Strength to Weight ratio
- Increase Stiffness to Weight ratio

### Round 1: 
The purpose of Round 1 was to determine the starting conditions for the bracket, and whether which parameters would achieve convergence given only a change in mesh size. 

### FEA Round 1
| Parameter | FEA 1 (Coarse) | FEA 1 (Fine) |
|:--|:--:|:--:|
| Max Stress (MPa) | 3.27 MPa | 4.18 MPa |
| Stress Location | <img width="350" alt="Round 1 Stress Analysis Medium Mesh" src="https://github.com/user-attachments/assets/417525b7-212b-4d3c-bf5b-e588a79ea28e" /> | <img width="350" alt="Round 1 Stress Analysis Fine Mesh" src="https://github.com/user-attachments/assets/831148d1-1c77-4d09-9697-baf84107799c" /> |
| Max Deflection (in) | 3.46e-5 in | 3.45e-5 in |
| Deflection Location | <img width="350" alt="Round 1 Mid Mesh Displacement" src="https://github.com/user-attachments/assets/9274daad-fcf5-41a0-870e-2e3da6924186" /> | <img width="350" alt="Round 1 Fine Mesh Displacement" src="https://github.com/user-attachments/assets/79cdfbc2-6f4d-424a-ad7a-af49b7ad338e" /> |
| Mass (lb) | 0.07 lb | 0.07 lb |
| Minimum Safety Factor | 247.26 | 197.81 |

### Convergence Check: 
I inputted all convergence values using this equation. 
  *C(a,b)=(2\operatorname{abs}(b-a)/(a+b))*100*
b represents X final. a represents x initial.  

#### Convergence Results 
| Metric | Convergence |
|:--|:--:|
| Deflections | 0.376% |
| Stresses | **21.75%** |
| Factor of Safety (FOS) | **22.22%** |

*Note: These values did not deviate by greater than 0.1% with repeated testing.* 

Results: 
Deflections converged nicely, but stresses did not. The goal for further rounds of FEA is to optimize the stresses to get as close to converging as possible. 
  The Factors of Safety not converging is less important due to both values being vastly above our desired safety factor of 4, but convergence of FOS is intended as well. 

### Round 2: 
The purpose of Round 2 was to achieve convergence in the stress values, as well to reduce the stress concentrations happening within the model. 

Pre-Test: Symmetric Filets with a radius of 0.05in were added at the corners of feature B as well as the rounded edge of feature A. 

<img width="2515" height="1437" alt="Pre Round 2 Fillet Addition" src="https://github.com/user-attachments/assets/ca94a05f-2396-44d8-a8d7-cf87657b3bea" />
<img width="2527" height="1400" alt="Pre Round 2 Chamfer Addition" src="https://github.com/user-attachments/assets/f6ff1003-dfd0-4892-8c27-e5c912d94377" />


### FEA Round 2
| Parameter | FEA 2 (Coarse) | FEA 2 (Fine) |
|:--|:--:|:--:|
| Max Stress (MPa) | 3.84 MPa | 4.22 MPa |
| Stress Location | <img width="350" alt="Round 2 Mid Mesh Stress" src="https://github.com/user-attachments/assets/d72bb7b0-08fa-46ea-bb3b-38009ff5b662" /> | <img width="350" alt="Round 2 Fine Mesh Stress" src="https://github.com/user-attachments/assets/e5b10ea3-0e6c-47eb-a6f9-8296de0786f9" /> |
| Max Deflection (in) | 3.46e-5 in | 3.45e-5 in |
| Deflection Location | <img width="350" alt="Round 2 Mid Mesh Displacement" src="https://github.com/user-attachments/assets/29dafa78-8495-45f5-b6c9-cfac8dfc317b" /> | <img width="350" alt="Round 2 Fine Mesh Displacement" src="https://github.com/user-attachments/assets/e179ac4b-5d89-4732-9d63-f41ff0924298" /> |
| Mass (lb) | 0.07 lb | 0.07 lb |
| Minimum Safety Factor | 215.10 | 200.76 |

#### Convergence Results 
| Metric | Convergence |
|:--|:--:|
| Deflections | 0.293% |
| Stresses | 7.059% |
| Factor of Safety (FOS) | 6.897% |
*Note: These values did not deviate by greater than 0.1% with repeated testing.* 


### Convergence Check: 
I inputted all convergence values using this equation. 
  *C(a,b)=(2\operatorname{abs}(b-a)/(a+b))*100*
b represents X final. a represents x initial.  

Convergence Results for Round 2: 

Convergence of Deflections: 0.376%
Convergence of Stresses = **21.75%**
Convergence of FOS = *22.22%*

Adding the chamfers into the design significantly decreased the variation within both the stresses and safety factors within the model. 

### Round 3: 
The purpose of Round 3 was to further tune the convergence in the stress values, as well as increasing the strength-to-weight, stiffness-to-weight, and location of stress concentrations. 

Pre-Test: At first I removed a considerable amount of material from the center of my bracket. The hope was for this to preserve the integrity of the model while reducing weight. This caused a catastrophic change in my models integrity, dropping the smallest factor of safety to 19. 

I scrapped this proposed change and instead added 20 degree filets to the corners where stress concentrations where occurring previously.  

<img width="2460" height="1400" alt="Round 3 Material Removal" src="https://github.com/user-attachments/assets/6c66e444-3d7f-4f7b-8cd6-19fe2acadb71" />
<img width="2460" height="1430" alt="Round 3 Cut " src="https://github.com/user-attachments/assets/1446e843-07ff-4761-a9b0-96a66a03b30b" />

Finalized Changes: 
<img width="2435" height="1485" alt="image" src="https://github.com/user-attachments/assets/ef5aa81b-dc10-49e4-aede-2f7b0ed3e319" />

Analysis 3 Notes: 
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

### FEA Round 3
| Parameter | FEA 3 (Coarse) | FEA 3 (Fine) |
|:--|:--:|:--:|
| Max Stress (MPa) | 3.91 MPa | 4.281 MPa |
| Stress Location | <img width="350" alt="Round 3 Mid Mesh Stress" src="https://github.com/user-attachments/assets/a949dbf4-2ea7-416e-83ab-304ef348d6cd" /> | <img width="350" alt="Round 3 Fine Mesh Stress" src="https://github.com/user-attachments/assets/c31120f0-c3da-40d8-827a-4a6872f585e7" /> |
| Max Deflection (in) | 3.27e-5 in | 3.32e-5 in |
| Deflection Location | <img width="350" alt="Round 3 Medium Mesh Displacement" src="https://github.com/user-attachments/assets/78ceb1a3-649d-464e-9d0f-9ee72eda20aa" /> | <img width="350" alt="Round 3 Fine Mesh Displacement" src="https://github.com/user-attachments/assets/9357308c-9e32-43b9-8568-982229b0e631" /> |
| Mass (lb) | 0.07 lb | 0.07 lb |
| Minimum Safety Factor | 211.53 | 193.26 |

#### Convergence Results (Fine Mesh)
| Metric | Convergence |
|:--|:--:|
| Deflections | 0.157% |
| Stresses | 1.08% |
| Factor of Safety (FOS) | 9.03% |

Significantly more accuracy between deflection and stress convergence when filets were added. Alongside this, the strength/weight ratio was increased with stiffness/weight as model weight did not increase by more than 0.001 lbs while yielding better results. 

*Note: These values did not deviate by greater than 0.1% with repeated testing.* 



## Decide


## Communicate

