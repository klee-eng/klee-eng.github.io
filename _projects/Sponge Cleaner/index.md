
---
layout: post
title: Sponge Cleaner
description:  This project was made for my junior design class, where we were given a budget of $150 and 6 weeks to make something useful. I  heavily contributed to both the electrical and mechanical components, including handling motor integration, circuit design, Arduino programming, lead screw design, and housing.
skills: 
- SolidWorks
- 3D Printing
- Rapid Prototyping
- Arduino
- Laser Cutting
main-image: /JuniorDesignProject.jpg 
---

## Overview
The submersible was designed with the intention of picking up and removing golf balls from lakes. It was equipped with two large syringes to control buoyancy, two PMDC motors with propellers, and a waterproof 180 degree servo. Weights were stuffed inside to account for the air stored within. Due to budget constraints, the project was primarily made out of spare parts and laser cut acrylic. 

{% include image-gallery.html images="OpenDownView.PNG, motormount.jpg" height="300" %} 
View of rack and pinion syringes and 3D printed motor mounts

---

## Claw
The claw was cut from acrylic and modeled after a claw machine game, where a single linear input results in the actuation of all arms at once. This had to be prompted from inside the submersible, so servo wires were routed and sealed inside so the servo rotation could pull the arms together. 

{% include image-gallery.html images="HoldingGolfBall.jpg" height="300" %} 
View of claw after actuation

---

## PCB
I designed and manufactured a PCB to mount the propeller motor drivers and interface directly with the Arduino Uno used. Screw terminals were used to connect the PCB to the syringe motor drivers and servo. The system was powered using 8 AA batteries in series. Commands were sent to the Arduino through keyboard presses to control the device and actuate the claw. 
 
{% include image-gallery.html images="SLD.png, PCBSub.png, HoldingPCB.jpg" height="300" %} 
Single-Line Diagram and PCB outline

---
