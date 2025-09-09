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

<p><i>Front (left) and back (right) of complete prototype.</i></p>

## Camera

This project provided an opportunity to integrate a camera into a robotic system using Python. The camera detects hands through the OpenCV and MediaPipe libraries, and computes the hand’s position relative to the center of the frame. This information is then used to calculate the motion required for the arm to center the hand. The camera is mounted on a custom-designed, detachable mount that uses neodymium magnets for easy attachment to the arm.

<div style="display: flex; gap: 10px;">
  <img src="/images-arm/camera_mount.jpg" height="300" alt="Hub1">
  <img src="/images-arm/camera_close_up.jpg" height="300" alt="Hub1"></div>

<p><i>Detached (left) and attached (right) camera mount.</i></p>

---

## Software

The chassis consists of two large aluminum platforms connected by four 0.5-inch steel bars, with two aluminum motor mounts attached to the underside of the base platform. All components were manufactured in-house: the platforms were cut using a waterjet, while the motor mounts were machined using CNC processes. Finite element analysis (FEA) was performed on all load-bearing components to verify safety and durability, ensuring the chassis can support the target maximum load of 200 lbs.

<div style="display: flex; gap: 10px;">
  <img src="/images-arm/arm_rqt_graph.jpg" height="400" alt="Hub1">
</div>

<p><i>Final chassis design: completed chassis assembly (left) and major components after waterjet cutting (right).</i></p>

---
