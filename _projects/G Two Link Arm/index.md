---
layout: post
title: Two-Link Robot Arm
description:  This project is a two-link robotic arm equipped with a camera at the end effector. The arm tracks and follows a human hand in real time. I developed this project as a hobby after graduating from UCSB to practice and extend my undergraduate engineering skills, while also gaining hands-on experience with ROS2.

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

All mechanical components were designed in Fusion 360 and 3D-printed using PLA. The system integrates an Arduino Uno, a 16-channel servo driver, a USB camera, and two servo motors: a 180° high-torque motor and a 360° high-speed motor with Hall effect sensor feedback. The continuous-rotation servo is controlled via PID through the Arduino to achieve accurate positioning. As a next step, I plan to design a larger base to house and manage the electronics and wiring.

<div class="image-row">
  <img src="/images-arm/front_active.jpg" alt="Hub1">
  <img src="/images-arm/circuit.jpg" alt="Hub2">
</div>

<p><i>Front (left) and back (right) of prototype.</i></p>

## Camera

The project involved integrating a camera into the robotic system using Python. The camera detects hands through the OpenCV and MediaPipe libraries, and computes the hand’s position relative to the center of the frame. This information is then used to calculate the motion required for the arm to center the hand. The camera is mounted on a custom-designed, detachable mount that uses neodymium magnets for easy attachment to the arm.


<div class="image-row">
  <img src="/images-arm/camera_mount.jpg" alt="Hub1">
  <img src="/images-arm/camera_close_up.jpg" alt="Hub2">
</div>

<p><i>Detached (left) and attached (right) camera with mount.</i></p>

---

## Software and ROS2

The software system was developed in ROS 2 using Python and consists of three nodes: a camera node that publishes hand position data, a kinematics node that calculates the joint angles required to move the arm, and an Arduino communication node that manages serial communication with the Arduino to control the servos. Nodes communicate through ROS 2 topics, and the system architecture is shown in the rqt_graph screenshot below.


<div class="image-row">
  <img src="/images-arm/arm_rqt_graph.jpg" alt="Hub1">
</div>

<p><i>Rqt_graph of ROS2 nodes.</i></p>

---
