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

</details>

---

<details>
  <summary><strong>Design Choices and Design Methods</strong></summary>

## Electronics
Since the time frame was quite short, many decisions were make quickly although they may not have been the most optimal choice in hindsight. 

We chose to use FRC motors and controllers because they are readily available, come with many complementary components that accelerate prototyping, and provide substantial torque without the need for industrial-grade motors.

We also believed that using CAN communication with the FRC motor controllers would give us greater flexibility in system integration and control.

The following is the rough schematic we followed for the electronics of the robot:

![The Electronics Schematic!](/assets/images/Electronics-Schematic.png)


## Gearbox Sizing
Although the motors were fairly strong, a gearbox was still required to reach the desired output torque and protect upstream electronics from burning out. 

Torque and RPM at peak power were used, assuming the motor would operate near this point under load.

The reduction was calculated based on the goal of traveling from endpoint to endpoint in under one second.

A 20% margin was added to the peak rpm then divided by the desired 60 rpm resulting in a 187:1 desired gear reduction. The reduction on the actual robot was brought down to 120:1 since the arm lengths were reduced with ample torque.

$$
Gear Ratio = \frac{9370 * 1.2}{60} = 187.4
$$

## Part Selection
Many of the components for the robot were selected spontaneously based on availability and cost.

The main structural aluminum was sourced from the remnant section at Industrial Metal Supply, where we found an 8-foot piece of 6x2-inch 6061 tubing for $40.
The carbon fiber tubes, aluminum round tubing, and bearings were purchased from Amazon, chosen for their convenient sizes and affordability at the time.


</details>
