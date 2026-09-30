# A6 – Bracket Drawing

## Objective
The objective of this project is to properly utilize engineering drawings in order to demonstrate design intent. 

## Analyze

From the previous assignment, the task was to design a bracket to withstand a certain force while holding a strap. 

A few changes were made to the bracket from the last week. 

Firstly, A error in calculations were discovered, the width in features D and E were about ten times thicker than necessary, this is because of a decimal error. 

Secondly, an error in dimensional analysis(specifically converting between the metric and imperial system) caused the diameter of Feature A to be 63% larger than required. 

These errors are corrected and are not reflected in the current drawings. 

### Parametric Design: 

Firstly, I had to ensure that the model was fully parametric. This was to ensure the model was able to adapt given any arbitrary change in material or constraints. 

<img width="1670" height="500" alt="image" src="https://github.com/user-attachments/assets/a6f3de63-1382-4c16-a3bc-2c3ce70c1de5" />
<img width="1667" height="445" alt="image" src="https://github.com/user-attachments/assets/0fda3429-3306-4e3d-8011-6ed0ff6dfd2f" />

I only entered the equations of the *governing* constraint, whether that be strength or stiffness. This reduced redundancy in the model. 

### Modeling 

I now began to model the part. 

I constructed feature A by extruding a circle and connecting my "diaA" variable to that dimension. The length of 1.50 was attached to the "FeatAL" variable

<img width="1962" height="1480" alt="image" src="https://github.com/user-attachments/assets/0d9eecda-3350-49bc-a448-b0c85892f7e2" />

Feature B was constructed by extruding a rectangle on the backside of Feature A. The length of B was a assumed dimension and the thickness of B was tied parametrically 

<img width="1947" height="1442" alt="image" src="https://github.com/user-attachments/assets/bc8c8fb0-d0c7-4278-a7e1-8f006beec00a" />

Feature C was constructed by extruding a rectangle on the center of the top surface of Feature B. Both the length and thickness of C is constrained parametrically 

<img width="1550" height="690" alt="image" src="https://github.com/user-attachments/assets/4e8d020c-f487-4b96-8e23-0a8b4c2bdd71" />

Feature D was made by extruding two rectangles on each side of Feature C. All dimensions of Feature D were constrained parametrically. 

<img width="1450" height="1187" alt="image" src="https://github.com/user-attachments/assets/53c8f0bc-4f64-4cb9-aeac-b64d1161e8c7" />

Lastly, Feature E was created by extruding two rectangles inward. All associated dimensions were constrained parametrically 

<img width="1187" height="1052" alt="image" src="https://github.com/user-attachments/assets/4ab01db7-490b-4e01-80aa-60b74eb91934" />

Here is the finished bracket: 

<img width="947" height="1095" alt="image" src="https://github.com/user-attachments/assets/5f12cc44-c0d1-43bf-b0f1-0d4275e27a5b" />

The CAD File can be viewed [here](https://github.com/VictorGaskin/Designs-Project-Portfolio-/blob/main/Bracket%20Draft.SLDPRT)

### Drawing 

Once my bracket was fully designed, I created a drawing file in SolidWorks. I ensured that the drawing was in Third Angle Projection as intended. This required a top view, front view, right view, and isometric projection. These views helped ensure ease of understanding and readability.  I To create the tolerances, I made sure that there was enough clearance so that the bracket would smoothly slide through the T beam. 

<img width="1307" height="1015" alt="image" src="https://github.com/user-attachments/assets/fac6e500-7a05-41b4-a0c1-cc9407f98b3a" />

The Drawing File can be viewed [here]()
### Fastening Plane 

I created this part by connecting two parallel lines with tangent arcs, I then dimensioned the correct distances, extruded the part to desired thickness, and then extruded cut holes into the fastening plane. 

<img width="1125" height="1137" alt="image" src="https://github.com/user-attachments/assets/c30e85dd-b18d-46ad-a65a-35c6b32a7a8f" />

### Fastening Plane Drawing

After the model was created, I created a engineering drawing, following the same parameters as the bracket drawing. 

<img width="1777" height="1375" alt="fastening plane drawing " src="https://github.com/user-attachments/assets/de1291da-0e55-47b1-ad18-cbb02d2262f7" />



## Decide


## Communicate

