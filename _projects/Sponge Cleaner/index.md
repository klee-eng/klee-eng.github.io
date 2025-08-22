---
layout: post
title: Sponge Cleaner
description:  This project was made for my junior design class, where we were given a budget of $150 and 6 weeks to design, prototype, fabricate, and test a device. I heavily contributed to both the electrical and mechanical components, including handling motor integration, circuit design, Arduino programming, lead screw design, and housing design.
skills: 
- SolidWorks
- 3D Printing
- Rapid Prototyping
- Arduino
- Laser Cutting
main-image: /JuniorDesignProject.jpg
main-image-height: 200

---

## Overview
This sponge cleaner is a countertop kitchen device designed to prevent the growth of bacteria and mold on sponges used for washing dishes. When a sponge is placed inside the device, pressing a button activates the cleaning process. The sequence begins with a PMDC motor-driven leadscrew that compresses the device walls to squeeze water out of the sponge, followed by a fan that continues to dry the sponge for 15 minutes. The device includes an Arduino Uno, and it is constructed from 3D-printed PLA and laser-cut acrylic components.

{% include image-gallery.html images="JuniorDesignCAD.jpeg" height="300" %}
Isometric view of final CAD assembly

---

## Prototypes
Major breakthroughs in the project were made following the creation of the leadscrew prototype and the circuit prototype. Due to budget constraints, rather than buying a lead screw, a custom lead screw was created using a modified screw and a skateboard bearing. The compressive wall was then glued to one end of the screw and a timing belt pulley was glued to the other end. The lead screw could then be driven by a belt that connected the pulley on the screw to the pulley on the motor.

The second major prototype for this project was the circuit prototype which integrated all of the major electrical components of our system. These components included a PMDC motor, a motor driver, a DC fan, an Arduino Uno, and a 6V power suppy. This protype was important for refining our code, and ensuring the drying sequence would function as desired.


{% include image-gallery.html images="JuniorDesignPrototypes.jpg" height="300" %}
Lead Screw Prototype and Circtuit Prototype
