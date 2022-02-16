# Wheel Clamping Robot
Mechatronics engineering project to design and fabricate an autonomous mobile robot with dual arm manipulators to identify and perform wheel clamping on illegally parked/ double parked cars.

This project was done by:
1. [Timothy Chelelgo](https://www.linkedin.com/in/timothy-chelelgo-49872222b/)
2. Nataly Musilah
3. Felistar Wambui
4. [Mark Maara](https://linkedin.com/in/mark-maara-42b235153/)

## Overview
The design focuses on a robot that employs computer vision to identify illegally parked cars or any parking infractions such as double parking, parking in a restricted zone without permission and parking in a way that causes congestion. Upon identification of any parking misdeed, the robot automatically clamps the motor vehicle and notifies a tow truck about collection at a stipulated time.

## Mechanical components
### Platform and chassis

To build the base of the robot we decided to use Steel for its properties of wear resistance and resistance to harsh weather conditions. The Steel also ensures that the robot will be able to handle heavier weights.

### Wheels

As the robot moves on asphalt, the tire material decided on was rubber for improved grip. The rubber component also presents a lower rolling resistance. 
The wheels have been made of aluminum alloy due to its corrosion resistance. Aluminum is also lighter than steel and hence ensures a smoother ride. Since they are stronger than steel, the have an added advantage of increased damage resistance.
### Clamp

After considering most of the clamps present in the market, it was agreed upon that the robot needed its own newly designed clamp that would work easily in tandem with it. 
Our design incorporates retractable links to provide a considerable grip on the wheel. 
The material used is steel.
## Navigation Method

The 2 front wheels are driven by motors relying on the differential method of steering. This is where the two front wheels share a common axis of rotation and the velocity of each wheel is varied for maximum maneuveribility. This steering system also ensures that there isn’t a need for any additional steering mechanism. 
### How Distance Is Calculated 
Through the use of reflectance sensors that measure the number of wheel revolutions.

## Electrical and electronic components
### Motors
Servo motors have many reasons for being used in a robotic arm, with the main reason being that the servo motor’s position, velocity and torque can be controlled as required which is necessary when building a robotic arm.
For this reason the design included the use of 10 servo motors in the robotic arms. 
Amongst those considered for the design was Hasyond 4.8V but we settled on the OEM small 42mm 450 rpm 30kgcm torque motors. These are suitable for the required speed of 450rpm.
The clamp also incorporates a servo motor for gripping.  
### Sensors
#### Sensors for obstacle detection: 
Infrared sensors positioned at the front section of the robot are used. There is no need for sensors at the back as the robot does not go in reverse. The IR sensor has an emitter and a photo transmitter that can detect up to distances of 80cm with the aid of a potentiometer. 
#### Sensors for distance calculation
Reflectance sensors were used to calculate the distance traveled through the number of wheel revolutions detected. 
#### Stepper motors
Stepper motors are included in the design to assist the robotic arms in motion greater than 1800. 
A total of 6 stepper motors were incorporated.
## Software implementation
Various software was used to aid in the design process. Most of the programming was done in python for the electrical components on Proteus. 
For the mechanical parts, Inventor was utilized to design draw and assemble the robot. 
The stress analysis was also done on Inventor. 
AI is included in the software to be developed for identifying illegally parked cars and also identifying and recognising the wheels that the robot is supposed to clamp.
### Computer vision
In order to identify illegally parked cars and their wheels so as they can be clamped, we used the SSD Mobilenet V2 FPNLite 320 by 320 pretrained model from the tensorflow model zoo because it is fast and not very resource heavy and so will be perfect for being deployed on a raspberry pi.
A video demonstration of the wheel detection is shown below

[![wheel](https://user-images.githubusercontent.com/68475422/154278470-05b42c7e-1e0b-466f-b8ea-b44193c9797d.png)}](https://youtu.be/PrjFQIVXV1U)
