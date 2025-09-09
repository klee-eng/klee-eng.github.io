---
layout: post
title: Two-Link Robot Arm
description:  This project was made for my Senior Capstone Project, where my team was given a budget of $5,000 and 9 months to design, prototype, fabricate, and test a cause-and-effect vehicle for infants and children with severe mobility impairments. As the mechanical design lead I led the design and fabrication of the chassis, motor mounts, and electrical enclosures. I also heavily contributed to the implementation and integration of the electrial system.
skills: 
- Fusion360
- 3D Printing
- Rapid Prototyping
- Arduino
- System Integration
- ROS2
- Python

main-image: /front.jpg

---

## Design Overview
This cause-and-effect vehicle for infants and young children is designed for use under the strict supervision of a licensed pediatric physical therapist. The vehicle responds to inputs from either the child’s controls or a therapist-operated controller located at the rear of the device, allowing it to move forward, backward, or spin in either direction. It is suitable for children ages 2–7 with varying levels of disability and can accommodate users weighing up to 200 lbs.


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
  <img src="/images-arm/arm_rqt_graph.jpg" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_NEW_CHASSIS.jpg" height="300" alt="Hub1"></div>

<p><i>Final chassis design: completed chassis assembly (left) and major components after waterjet cutting (right).</i></p>

---

  <img src="/images-capstone/CCS_ME 2024 MOTORS.jpg" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_ME Capstone 2024_BATTERY.jpg" height="300" alt="Hub1"></div>

<p><i>Locations of motors and battery: motors mounted underneath the chassis (left) and e-bike battery slides in and out of the connector beneath the seat (right).</i></p>
