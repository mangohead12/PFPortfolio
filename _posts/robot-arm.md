---
layout: project
title: "6 DoF General Purpose Robot Arm (WIP)"
image: /assets/images/
video: https://youtube.com/…
permalink:/projects/robot_arm/
---

## Project: 6-DoF Robotic Arm
The robot arm was a group project with four other students. 
The goal was to create a robotic arm with the goal of making mixed drink to order within a 13 week period. 
I was responsible for the mechanical design, fabrication and elecronics planning for this project.

As of right now, the first three degrees of freedom are complete but the last three for orientation at the end of the arm is still in progress. 

![The Robot Arm So Far!](/assets/images/Robot-Arm.png)

---

<details>
  <summary><strong>The Design</strong></summary>

## Design Goals
The following were some goals that were determined before the design phase:
- The robot shall be compatible with ROS2
- The robot should be capable of moving from one end point to the other within one second
- The robot should be capable of holding and moving a 2 pound payload at the end of the arm
- Robot parts shall be manufacturable in house or purchaseable online
- The Robot should have a workspace of 6 feet accross

## Subsystems

The robot arm is divided into two subsystems, the positional subsystem and the orientation subsystems. Where the positional is a 3DoF articulated robot and the orientation subsystem is a quaternion wrist (WIP).

## Design Considerations for the First 3 DoF
Since the time frame was quite short, many decisions were make quickly although they may not have been the most optimal choice in hindsight. 


