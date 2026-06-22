---
layout: post
title: Terrain Simulator
description:  This project was completed for my haptics class, where the final assignment was to design and build a haptic device that a user can interact with. The project was open-ended, allowing for creative interpretation of what kind of haptic experience to create.
skills: 
- Rapid Prototyping
- Arduino IDE
- 3D Printing
- Fabrication
- MATLAB
- Python
  
main-image: /terrain_simPic (1).jpeg
---

## Mechanical Design

The terrain simulator was designed to generate at least 15 lbf of vertical force at the end effector throughout the desired workspace. A 5-bar pantograph-style linkage was selected as the primary mechanism. To determine the required workspace for simulating a walking motion, a participant's stride length was measured while seated in a chair similar to the one intended for the final device. Based on these measurements, a linkage consisting of a 5 in ground link, 6 in proximal links, and 9.5 in distal links was determined to provide the required workspace of approximately 14 in in length and 5 in in maximum vertical travel while maintaining an elbow-out configuration.

A vertical end-effector force of 15 lbf was determined to be sufficient for simulating the sensation of stepping on a solid surface. After the linkage dimensions were established, a Python script was developed to analyze the mechanism's Jacobian and calculate the actuator torques required at the base joints to produce this force throughout the workspace. The analysis showed that approximately 15 N·m of torque was required from each actuated joint to achieve the desired end-effector force across the entire operating range.

The motors selected for the system were repurposed from an electric skateboard and were rated for a continuous torque of 5 N·m. To meet the torque requirements, a belt-drive transmission with a 5:1 reduction ratio was incorporated into the design. This transmission increased the available joint torque beyond the required 15 N·m while also providing additional force capacity for simulating more complex virtual terrain features beyond a flat walking surface.


## Electrical and Control System

The electrical and control system was built around a Teensy 4.1 microcontroller, which served as the central controller for the terrain simulator. The device was actuated by two BLDC motors driven by independent VESC motor controllers. Desired joint torques were computed by the Teensy and transmitted to each VESC through a UART communication interface. The VESCs then handled the low-level current control and motor commutation required to produce the commanded torques.

Each motor contained integrated Hall-effect sensors that provided rotor position feedback for motor commutation. To accurately measure the position of the mechanism itself, ATM10 open-center rotary encoders with a resolution of 2048 pulses per revolution were mounted directly to the base joints of the 5-bar linkage. These encoders provided precise measurements of the joint angles, allowing the controller to determine the configuration of the mechanism and compute the corresponding end-effector position.

The control firmware was developed on a Teensy 4.1 microcontroller and executed the real-time control loop responsible for rendering virtual terrain to the user. Joint angle measurements from the base encoders were used to compute the configuration of the 5-bar linkage through forward kinematics, allowing the controller to determine the position of the end effector within the workspace.

Virtual objects were rendered using an impedance control framework. Based on the position of the end effector relative to objects in the virtual environment, the controller computed the desired interaction force that the user should experience. The required torques at each actuated joint was then computed from these forces using the Jacobian transpose of the mechanism.

The desired joint torques were converted into motor current commands and transmitted to the VESC motor controllers via UART. The VESCs then regulated motor current to generate the required torque, allowing the system to accurately reproduce forces associated with virtual terrain features and obstacles.

## Virtual Environments

A collection of virtual environments was developed to enable user interaction with the device. Five static environments were implemented: a flat ground surface, a vertical wall, a stationary box obstacle, an inclined ramp, and a mud environment. The mud environment combined a compliant ground model with a layer of linear damping to simulate the resistance encountered when walking through soft terrain.

Two dynamic environments were also developed. The first simulated an impact surface by augmenting the contact force model with a decaying sinusoidal term following contact, producing a transient vibration similar to striking a rigid object. The second environment enabled continuous walking over a repeating sequence of box obstacles, allowing users to experience varying terrain elevations without reaching the limits of the physical workspace.

Together, these environments demonstrated the system's ability to render both static and dynamic terrain features while providing realistic force feedback through the 5-bar linkage mechanism. A demonstration of the device can be viewed in the video below.

<iframe 
  src="https://drive.google.com/file/d/1V9EGMr26LJHOM8wLXtdLaSR-3ou_T9Hb/preview"
  style="aspect-ratio: 16 / 9; width: 100%; height: auto; border: 0;"
  allow="autoplay">
</iframe>

<p><i>Video demonstration of the Terrain Simulator</i></p>

