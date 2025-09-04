---
layout: post
title: Cause-and-Effect Vehicle
description:  This project was made for my Senior Capstone Project, where my team was given a budget of $5,000 and 9 months to design, prototype, fabricate, and test a cause-and-effect vehicle for infants and children with severe mobility impairments. As the mechanical design lead I led the design and fabrication of the chassis, motor mounts, and electrical enclosures. I also heavily contributed to the implementation and integration of the electrial system.
skills: 
- SolidWorks
- 3D Printing
- Rapid Prototyping
- Arduino
- System Integration
- GD&T
- Soldering
main-image: /CCS_ME Capstone 2024_CONRTOLLER.jpg

---

## Description
This cause-and-effect vehicle for infants and young children is designed for use under the strict supervision of a licensed pediatric physical therapist. The vehicle responds to inputs from either the child’s controls or a therapist-operated controller located at the rear of the device, allowing it to move forward, backward, or spin in either direction. It is suitable for children ages 2–7 with varying levels of disability and can accommodate users weighing up to 200 lbs.

<div style="display: flex; gap: 10px;">
  <img src="/images-capstone/CCS_ME_Capstone_2024_FULL.jpg" height="300" alt="Hub1">
</div>

<p><i>Image of completed cause-and-effect vehicle.</i></p>

---

## User Controls

Because cerebral palsy can present differently from case to case, five control nodes are positioned at various locations around the vehicle, enabling the child to operate it with their hands, feet, or head. Each control node can be fitted with either a joystick or a set of four buttons, depending on the child’s needs. The vehicle is operated by pressing a button or moving the joystick. The movement associated with each button is determined by the input jack on the control node to which the button is connected.

<div style="display: flex; gap: 10px;">
  <img src="/images-capstone/CCS_JOYSTICK.png" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_ME Capstone 2024_HUB.jpg" height="300" alt="Hub1"></div>


## Physcal Therapist Controls

The supervising physical therapist has two methods of controlling the vehicle: the main controller mounted at the rear and a remote stop button. Both inputs override the child’s controls to ensure safety. The main controller is equipped with a two-axis potentiometer joystick for directional movement, two potentiometers to adjust the speed and duration of the child’s inputs, four mode buttons to define the types of movement permitted, and an emergency stop button. It also houses an Arduino Mega and a custom PCB for system control. The remote stop button, contained in a separate enclosure, activates the vehicle’s stop mode, during which the brakes engage and the motors cease receiving inputs. The remote operates reliably within a range of approximately 10 feet.

<div style="display: flex; gap: 10px;">
  <img src="/images-capstone/NEW_CONTROLLER.jpg" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_REMOTE_STOP.jpg" height="300" alt="Hub1"></div>

<p><i>Two methods of physical therapist controls: main controller (left) and remote stop button (right).</i></p>

---

## Chassis

The chassis consists of two large aluminum platforms connected by four 0.5-inch steel bars, with two aluminum motor mounts attached to the underside of the base platform. All components were manufactured in-house: the platforms were cut using a waterjet, while the motor mounts were machined using CNC processes. Finite element analysis (FEA) was performed on all load-bearing components to verify safety and durability, ensuring the chassis can support the target maximum load of 200 lbs.

<div style="display: flex; gap: 10px;">
  <img src="/images-capstone/ME CHASSIS.jpg" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_NEW_CHASSIS.jpg" height="300" alt="Hub1"></div>

<p><i>Final chassis design: completed chassis assembly (left) and major components after waterjet cutting (right).</i></p>

---

## Motors and Battery

The vehicle is powered by two 24V brushless DC integrated-wheel motors. For user safety, the motor speed is limited to 3.4 mph, while still providing sufficient torque to move the maximum target load of 200 lbs. Power is supplied by a 24V lithium-ion e-bike battery.

<div style="display: flex; gap: 10px;">
  <img src="/images-capstone/CCS_ME 2024 MOTORS.jpg" height="300" alt="Hub1">
  <img src="/images-capstone/CCS_ME Capstone 2024_BATTERY.jpg" height="300" alt="Hub1"></div>

<p><i>Locations of motors and battery: motors mounted underneath the chassis (left) and e-bike battery slides in and out of the connector beneath the seat (right).</i></p>
