---
tags:
  - CT
  - "#ADCS"
  - Evo-1
  - Simulation
  - "#PID"
aliases:
  - aerospace control teacher ke liye kaam
Status: work-in-progress
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

## 