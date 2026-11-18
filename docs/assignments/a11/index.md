# A11 – Motor Selection
The purpose of this assignment is to continue upon the leadscrew project to select and spec a proper motor for the strain gauge. This includes frame design and bearing design, ensuring the crosshead moves smoothly under designed torque and loads. 

## Objective

### Motor Selection: Victor Gaskin 

Before the calculations could proceed, I needed to recall the rotational speed range and Torque applied to a single leadscrew, then carry those values to help me ascertain the figures I needed to match in terms of selecting the motor. 

<img width="955" height="1280" alt="image" src="https://github.com/user-attachments/assets/59dcb88a-1b43-4efb-9117-66d73d71596c" />

As a result of the calculations, I ended up choosing a McMaster-Carr DC Gearmotor. There was multiple gearmotors to choose from but the majority of them either provided speed much larger than the safety factor would account for or a torque force that is significantly too large for leadscrews to sustain consistently. 
Chosen Motor: https://www.mcmaster.com/6409K17/

The aditional torque that this Gearmotor provides above the calculations would be sustained by the safety factor of which the leadscrew was chosen under, as it's diameter is larger than the diameter used for the calculations(i.e, it was calculated using the most conservative estimate under the highest expected loading conditions.) 

<img width="1050" height="811" alt="image" src="https://github.com/user-attachments/assets/3f61c596-1255-4897-9608-81976bb6ac19" />


The provided Speed-Torque Chart helped verify this decsion: 

<img width="1250" height="947" alt="image" src="https://github.com/user-attachments/assets/40e6ac0f-a9f5-42a1-b755-d25a38faa2f0" />



Motor Dimensions: 
Length: 3.5"
Width: 2.75"
Height: 3" 
Mounting Hole Locations
  Main Mount 1.86 in x 1.43 in
    Screw Holes at edges

### Motor Mount Design
(Note: the gearmotor provides a very generous mount already)

Through the calculations, the factor that determined the leading thickness was the bending moment(t = 2.34mm). Despite this, I choose to use a thickness of 4mm(approximately 1/8") in order to standardize the CAD Modeling process later 

#### Bending Moment Calculation

<img width="976" height="1280" alt="image" src="https://github.com/user-attachments/assets/44dcb89c-2a20-408b-ba9f-a183d89ab478" />

#### Deflection Thickness Calculation: Victor Gaskin 

<img width="1179" height="720" alt="image" src="https://github.com/user-attachments/assets/314cbf9f-9c91-41be-8f1a-c1f477ed37fd" />

#### Motor Mount Design: Victor Gaskin

Regarding the motor mount design, my initial concept was to have the mount align with the preexisting "mount" and only provide additional support and a metal surface to screw onto. Later in the design process, Derek further optimized this design in order to accommodate guiderails. 

<img width="608" height="613" alt="image" src="https://github.com/user-attachments/assets/111a9f9c-b931-4b2f-86c2-be869c74ea7a" />

#### Coupler Design: Victor Gaskin

I was tasked to calculate the minimum diameter that the coupler that would fit between the motor mount and the leadscrew. I needed to take into account that the diameter's between the "entrance" and "exit" holes on each side would have to differ, and that this would affect the calculations. 

These calculations would assist me in choosing a coupler: 
  The coupler I chose was: https://www.ruland.com/pcr16-6-5-a.html

(Note, the diameter of the larger entrance hole, which is where the leadscrew would be inserted into, was the driving diameter.) 

<img width="933" height="1280" alt="image" src="https://github.com/user-attachments/assets/7f56a662-d06b-453a-a8d9-334ae7e47e89" />

## Analyze


## Decide
_Reference your concept selection (Pugh matrix) here. How does this design follow from that decision?_

## Communicate
