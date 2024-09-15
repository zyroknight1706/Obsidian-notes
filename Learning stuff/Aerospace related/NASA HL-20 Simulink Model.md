---
tags:
  - CT
  - "#ADCS"
  - Evo-1
  - Simulation
  - "#PID"
aliases:
  - aerospace control teacher ke liye kaam
Status: Completed
---
 ***15-09-2024
18:43***
# *Main Content*⚠
-----

## Introduction

This model is basically a demo model already made by Mathworks for Simulink. It has a bunch of system dynamics already modelled, I'm still doing work on this, as she already told me herself that this thing will take time, I'm fine with it, but I just want to make sure that she doesn't think that I'm totally dumb, I think she does already. 

![[Pasted image 20240915185130.png]]

The model illustrates the NASA HL-20 lifting body airframe approach and landing flight phases using an automatic-landing controller.

For more information, see [NASA HL-20 Lifting Body Airframe](https://in.mathworks.com/help/aeroblks/nasa-hl-20-lifting-body-airframe.html)
So, the paper that MATLAB people used to write this model was 

## Intricacies of the model

So this model basically has the following parts to it:
- Simulink's specialised 3D model block (called UE visualisation)
- A whole output bus model where there are a shitton of scopes
- Sensor models block, which has the IMU, GPS and something known as an Altimeter.
- A Guidance system block, which I don't know how it works, I'll look into that later, or I'll open it up and check.
- Something known as an airdata system block, which, when I opened the block, is just a fucking filter, to take out two values lol
- The Control System which has like three types of controllers, first is the Classical Controller (which, I believe is the pole placement controller), and two different types of H-infinity Robust Controllers.
- The Actuators block, which is just using the Simulink Actuator block with some extra steps
- and of course, the Mathematical and dynamical model of the spacecraft.

## Outputs
After running the model in Simulink, first it didn't run, told me that the 3d simulation engine doesn't start. I didn't change anything, but I guess it was due to the fact that I was in Ubuntu, and my graphics card on Ubuntu barely runs.
So, I decided to change my OS to windows (Perks of having a dual-booted system ig 😎).

![[Pasted image 20240915214515.png]]

Lo and Behold, it works!

It gives a shitton of outputs and takes in a shitton of inputs too. I'm not sure how I will figure out a way to make a controller for this without killing myself

### Attitude Accelerations Mach

![[Pasted image 20240915215404.png]]

This is the graph we should get.

### Demands Vs. Achieved

![[Pasted image 20240915215453.png]]

### Inertial Position

![[Pasted image 20240915215535.png]]

### Limited Actuators

![[Pasted image 20240915215628.png]]

------
## References

[MATLAB Website for the Simulink Model of the Controller]([Explore the NASA HL-20 Model - MATLAB & Simulink - MathWorks India](https://in.mathworks.com/help/aeroblks/running-a-demo-model.html))
[Explanation of the HL20 Model itself]([NASA HL-20 Lifting Body Airframe - MATLAB & Simulink - MathWorks India](https://in.mathworks.com/help/aeroblks/nasa-hl-20-lifting-body-airframe.html))
[PDF Document if ever lost](19920021931.pdf)
