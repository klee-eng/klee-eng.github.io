---
layout: post
title: Two-Link Robot Arm
description:  This project is a two-link robotic arm equipped with a camera at the end effector. The arm tracks and follows a human hand in real time. I developed this project as a hobby after graduating from UCSB to practice and extend my undergraduate engineering skills, while also gaining hands-on experience with ROS 2.

skills: 
- Fusion360
- 3D Printing
- Rapid Prototyping
- Arduino
- System Integration
- ROS2
- Python

main-image: /cropped_front.jpg

---

## Design Overview
All mechanical components were designed in Fusion 360 and 3D-printed using PLA. The system integrates an Arduino Uno, a 16-channel servo driver, a USB camera, and two servo motors: a 180° high-torque motor and a 360° high-speed motor with Hall effect sensor feedback. The continuous-rotation servo requires PID control through the Arduino to achieve accurate positioning.


<div style="display: flex; gap: 10px;">
  <img src="/images-arm/front_active.jpg" height="300" alt="Hub1">
  <img src="/images-arm/circuit.jpg" height="300" alt="Hub1"></div>


## Camera Mount

The supervising physical therapist has two methods of controlling the vehicle: the main controller mounted at the rear and a remote stop button. Both inputs override the child’s controls to ensure safety. The main controller is equipped with a two-axis potentiometer joystick for directional movement, two potentiometers to adjust the speed and duration of the child’s inputs, four mode buttons to define the types of movement permitted, and an emergency stop button. It also houses an Arduino Mega and a custom PCB for system control. The remote stop button, contained in a separate enclosure, activates the vehicle’s stop mode, during which the brakes engage and the motors cease receiving inputs. The remote operates reliably within a range of approximately 10 feet.

<div style="display: flex; gap: 10px;">
  <img src="/images-arm/camera_mount.jpg" height="300" alt="Hub1">
  <img src="/images-arm/camera_close_up.jpg" height="300" alt="Hub1"></div>

<p><i>Two methods of physical therapist controls: main controller (left) and remote stop button (right).</i></p>

---

## Software

The chassis consists of two large aluminum platforms connected by four 0.5-inch steel bars, with two aluminum motor mounts attached to the underside of the base platform. All components were manufactured in-house: the platforms were cut using a waterjet, while the motor mounts were machined using CNC processes. Finite element analysis (FEA) was performed on all load-bearing components to verify safety and durability, ensuring the chassis can support the target maximum load of 200 lbs.

<div style="display: flex; gap: 10px;">
  <img src="/images-arm/arm_rqt_graph.jpg" height="400" alt="Hub1">
</div>

<p><i>Final chassis design: completed chassis assembly (left) and major components after waterjet cutting (right).</i></p>

---
