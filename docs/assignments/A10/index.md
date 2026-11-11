# A10 – Lead Screw Translating System

## Objective
The objective of this assignment was to analzye and a design and model a leadscrew alongside other components in order to create a analogue tensile loader than could consistantly measure 2kN forces. 

## Analyze
### LeadScrew Design: Victor Gaskin
The minimum dimensions for the leadscrew was found by applying the safety factor(4) to the yield strength of the stainless steel leadscrew(205 MPa) Each of the two screws supports a 1 kN design load, requiring
a minimum core diameter of 4.98 mm. 

<img width="768" height="1024" alt="image" src="https://github.com/user-attachments/assets/926a3e4e-01ac-4868-87e9-7f3936fa6501" />

The 3/8"‑12 Thread Acme stainless steel lead screw (McMaster‑Carr 95061A813) was selected because its root diameter of  7.5 mm more than satisfies the minimum diameter requirement. 

Following the calculations onward, the range of speeds that the leadscrew would undergo was to be determined
<img width="770" height="505" alt="image" src="https://github.com/user-attachments/assets/8d0e20d7-c7d0-45e5-a483-df70d2025590" />

Results: The Screw’s lead of 2.117 mm/rev produces a rotational speed range of 0.473–23.6 rpm


The next Step was to determine the amount of torque to be applied to one leadscrew 
Using the screw torque equation with a friction coefficient of 0.15, the torque per screw is 1 N·m, giving a total drive
torque of 2 N·m. This configuration ensures smooth, controlled motion and sufficient strength for
the 2 kN tensile load.
<img width="695" height="505" alt="image" src="https://github.com/user-attachments/assets/e782d2d0-c75f-48d9-adc9-306eb42c5e46" />

### Nut Design: Victor Gaskin

Through the choice of the leadscrew, I assumed a nut of a similar diameter to the leadscrew would have to be chosen. 

The nut’s 25 mm thread engagement provides approximately 12 engaged threads, distributing the 2 kN load evenly. This provides a considerable factor of safety as only about 4 engaged threads would be been required in order to properly distribute this load

The forces sustained on the bearing utilizing the bending stress equation reaches about 8 MPa, which is considerably below 932 Bearing Bronze's Yield Strength of 105 MPa. This ensures that these nuts can be properly loaded and considerably overloaded without risk of failure.

A 932 bearing‑bronze Acme flange nut (McMaster‑Carr 95120A592) was chosen to pair with the 3/8‑12 lead screw due to the results of the calculations. 

<img width="768" height="1024" alt="image" src="https://github.com/user-attachments/assets/fd010587-d8fd-4c14-9b9e-31dfa96deba9" />


### CrossHead Design: Victor Gaskin

The crosshead was analyzed through the  simply supported steel beam assumption. spanning 150 mm between the
two lead screws, with  load applied at midspan. Under the 4 kN design load, the
maximum bending moment is 45MPa( 45 N mm)  for 25 mm × 20 mm rectangular section—below the 250 MPa allowable stress for stainless steel.
The corresponding deflection under the 2 kN test load is 0.0437 mm, far less than the 0.1 mm limit,
this verifies that the crosshead maintains adequate stiffness. The selected geometry provides both strength and rigidity while keeping to a realistic size that the machine would be able to accomodate. 

Mounting holes at each end accommodate the bronze flange nuts, ensuring smooth transfer of load and lower stress concentrations 

This design achieves safe operation, minimal deflection, and streamlined assembly for repeatitious tensile tests. 

<img width="785" height="672" alt="image" src="https://github.com/user-attachments/assets/0dcc8fad-71f1-4ef2-9475-695a07700cbb" />

#### Sketch

<img width="725" height="270" alt="image" src="https://github.com/user-attachments/assets/a17d9150-32c8-4fe4-affc-c8c17c17f70a" />


### Table 
| Item Number | Quantity | Name | Cost/Item | Cost | Purchase Link |
|:-----------:|:--------:|:----:|:---------:|:----:|:-------------:|
| 1 | 2 | 18-8 Stainless Steel Acme Lead Screw | $64.53 | $129.06 | [Lead Screw]( https://www.mcmaster.com/95061A813/) |
| 2 | 2 | 932 Bearing Bronze Acme Flange Nut | $111.78 | $223.56 | [Bronze Nut](https://www.mcmaster.com/95120A592/) |
| 3 | 1 | x | $0.00 | $0.00 | [www.xx.com](https://www.xx.com) |
| 4 | 1 | x | $0.00 | $0.00 | [www.xx.com](https://www.xx.com) |
| 5 | 1 | x | $0.00 | $0.00 | [www.xx.com](https://www.xx.com) |
| | | | | **Total Cost** | **$0.00** |
## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate

