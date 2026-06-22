---
layout: post
title: Terrain Simulator
description:  This project was completed for my haptics class, where the final assignment was to design and build a haptic device that a user can interact with. The project was open-ended, allowing for creative interpretation of what kind of haptic experience to create.
skills: 
- Rapid Prototyping
- Arduino IDE
- 3D Printing
- Fabrication
- Matlab
- Python
  
main-image: /terrain_simPic (1).jpeg
---

## Design

The terrain simulator was designed to generate at least 15 lbf of vertical force at the end effector throughout the desired workspace. A 5-bar pantograph-style linkage was selected as the primary mechanism. To determine the required workspace for simulating a walking motion, a participant's stride length was measured while seated in a chair similar to the one intended for the final device. Based on these measurements, a linkage consisting of a 5 in ground link, 6 in proximal links, and 9.5 in distal links was determined to provide the required workspace of approximately 14 in in length and 5 in in maximum vertical travel while maintaining an elbow-out configuration.

A vertical end-effector force of 15 lbf was determined to be sufficient for simulating the sensation of stepping on a solid surface. After the linkage dimensions were established, a Python script was developed to analyze the mechanism's Jacobian and calculate the actuator torques required at the base joints to produce this force throughout the workspace. The analysis showed that approximately 15 N·m of torque was required from each actuated joint to achieve the desired end-effector force across the entire operating range.

The motors selected for the system were repurposed from an electric skateboard and were rated for a continuous torque of 5 N·m. To meet the torque requirements, a belt-drive transmission with a 5:1 reduction ratio was incorporated into the design. This transmission increased the available joint torque beyond the required 15 N·m while also providing additional force capacity for simulating more complex virtual terrain features beyond a flat walking surface.


## Electrical and Control System



Designed and built a 5-bar kinesthetic haptic device that simulates variable terrain underfoot for the lower limb, integrating BLDC motors, VESC controllers, incremental encoders, and a Teensy 4.1 microcontroller into a complete electromechanical system. Programmed five static and two dynamic virtual terrain environments using impedance control, allowing the device to render realistic, responsive resistance in real time rather than a fixed motion profile. Used Python to analyze joint torques and tune the system to deliver 15 lb of end-effector resistance across the full workspace. Mechanical components were modeled in Fusion 360 and fabricated through manual milling and 3D printing, taking the project from CAD concept to a working, tested prototype.

<iframe 
  src="https://drive.google.com/file/d/1V9EGMr26LJHOM8wLXtdLaSR-3ou_T9Hb/preview"
  style="aspect-ratio: 16 / 9; width: 100%; height: auto; border: 0;"
  allow="autoplay">
</iframe>

<p><i>Video demonstration of the Terrain Simulator</i></p>

