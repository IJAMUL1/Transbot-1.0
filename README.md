# Transbot_1.0

Since the introduction of the Ford Model T in 1908, advancements in transportation over many decades have coincided with tremendous improvements to the standard of living in human civilization. Self-driving/autonomous vehicles are on the cusp of being realized and their application in rendering humanitarian aid shall be essential. Vaccines and medical supplies could be delivered to hard hit areas during a pandemic without risking the spread of disease via the logistical chain. Food and water could be delivered to survivors of natural/ man-made disasters when volunteers are in limited supply. Our device, the Transbot 1.0, aims to simulate the operation of such an autonomous vehicle. The Transbot 1.0  is envisioned to do the following;
- To be a dispatch device to provide essential products to people living in areas affected by insurgency.
- To support delivery networks and preserve life by reducing the need for human contact therefore reducing spread of disease during a pandemic.

# Robot Demo
![Untitled video - Made with Clipchamp (8)](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/4dc2dc3c-5092-43a9-b7df-07fd5d63d5f8)

## Table of Contents

- [Introduction](#introduction)
- [Project Requirement](#project-requirements)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Setup Instructions](#setup-instructions)
- [Additional Notes](#additional-notes)
- [Code Structure](#code-structure)
- [Functionality](#functionality)
- [Usage](#usage)
- [Contributing](#contributing)

## Introduction

In this project, we address the challenge of designing an autonomous parking system capable of navigating a predefined path within a parking lot, detecting available parking spaces, and efficiently maneuvering to park in the first available spot. Our solution involves the use of an Arduino-based robot equipped with sensors to detect intersections, objects obstructing parking spaces, and indicators for successful parking. This documentation provides a comprehensive overview of the project's objectives, problem statement, scenario description, task requirements, deliverables, and additional resources for implementation. Whether you're a student, hobbyist, or enthusiast interested in autonomous robotics or tackling real-world challenges with Arduino, this documentation serves as a valuable resource to understand, replicate, and contribute to our project.

## Project Requirements

- Line Following Robot: The robot must accurately follow the path marked by black tape within the parking lot.
- Intersection Indication: Indicate when traversing intersections using LEDs.
- Object Detection: Detect objects obstructing parking spaces using a single ultrasonic sensor. Provide indication of object detection through LEDs and LCD displays.
- Parking Functionality: Successfully park in the first available parking space detected.
- Display of Occupied Spaces: Display the number of occupied parking spaces encountered before parking using LCD displays.

## Hardware Requirements

The hardware components required for the project, include:
- Chassis and mechanical components
- Arduino Uno
- 2 x Continous Servo Motors
- Pulolo Reflecance Sensor
- 2 x Ultrasonic Sensors
- Parallax 2 X 16 Serial LCD With Piezo Speaker 
- Power supply
- Breadboard
- Wires
- Leds
- Etc.

## Software Requirements

Specify all the software dependencies needed to run the project, including but not limited to:
1. Arduino IDE: The Arduino Integrated Development Environment (IDE) is required to compile and upload the Arduino code to the microcontroller board.

1. Arduino Libraries:
    - QTRSensors library: Used for controlling the QTR Reflectance Sensor for line following.
    - NewPing library: Used for interfacing with the ultrasonic sensor for object detection.
    - Servo library: Used for controlling the continuous servo motors for movement.
    - SoftwareSerial library: Used for communicating with the LCD display for output indication.
    - Arduino Board Package: Ensure that the appropriate board package is installed in the Arduino IDE to support the microcontroller board you are using (e.g., Arduino Uno, Arduino Nano).

## Setup Instructions
- Reflectance Sensor: The QTR Reflectance Sensor is used for line following. Calibration is performed to ensure accurate readings.
- Ultrasonic Sensor: NewPing library is used to interface with the ultrasonic sensor for object detection.
- Servo Motors: Servo library is utilized to control the continuous servo motors for movement.
- LCD Display: SoftwareSerial library is employed to communicate with the LCD display for output indication.

## Additional Notes:
Calibration of sensors is crucial for accurate readings and proper functionality.
LED indicators are used for visual feedback, and LCD display provides additional output information.
The system operates autonomously, following predefined rules and behaviors.

## Functionality:
- Line Following: The robot follows a predefined path marked by black tape using the QTR Reflectance Sensor.
- Intersection Detection: Intersections are detected using sensor readings, and appropriate actions are taken at each intersection.
- Object Detection: Objects obstructing parking spaces are detected using the ultrasonic sensor.
- Parking Maneuvers: The robot parks in the first available parking space, considering obstacles and following specific parking rules.

## Code Structure:
The code consists of setup and loop functions, where the main logic for sensor readings, intersection handling, and parking maneuvers is implemented.
Various functions are defined for specific actions such as line following, turning, parking, and obstacle indication.

## Usage:
Upload the provided Arduino code to the Arduino board.
Ensure all components are properly connected and calibrated.
Monitor the output using the serial monitor and LCD display.
Test the robot's functionality in a controlled environment to ensure proper operation.

