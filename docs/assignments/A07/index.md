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

### FEA Mesh Comparison

| Parameter | FEA 1 (Coarse) | FEA 2 (Fine) |
|:--|:--:|:--:|
| Max Stress (psi) |  |  |
| Stress Location | [View Image](<img width="1672" height="1402" alt="Round 1 Mid Mesh Stress" src="https://github.com/user-attachments/assets/9f27a97c-2b5c-4184-9633-00dc620983f2" />
) | [View Image](<img width="1700" height="1420" alt="Round 1 Fine Mesh Stress " src="https://github.com/user-attachments/assets/9fd02114-ad4a-49fa-9d5b-327a75c9b5b6" />
) |
| Max Deflection (in) |  |  |
| Deflection Location | [View Image](<img width="1687" height="1385" alt="Round 1 Mid Mesh Displacement " src="https://github.com/user-attachments/assets/b60e2435-6f4c-48f2-ada4-e627d00f4e26" />
) | [View Image](<img width="1695" height="1402" alt="Round 1 Fine Mesh Displacement " src="https://github.com/user-attachments/assets/9f7d95bb-1624-4db3-a5c4-8a41b2d696e0" />
) |
| Mass (lb) |  |  |
| Minimum Safety Factor |  |  |
| Safety Factor Location | [View Image]() | [View Image]() |
| Number of Mesh Elements |  |  |
## Decide


## Communicate

