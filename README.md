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

Here we develop a robot that can be controlled remotely and functions mainly to deliver essential packages to set locations. Hence, the spread of communicable diseases is hindered and supply-chain bottlenecks are avoided. The Transbot 1.0 operates in manual (RC) and autonomous modes. It interfaces with a mobile-application-based user interface and can be sent to specific locations to deliver packages. The transbot contains a Pololu QTR-8RC Reflectance sensor that enables it to remain centered as it follows the track during autonomous operation. It also contains a Bluetooth module that enables it to interface with the Transbot_UI application through serial UART communication during manual/ RC mode.

## Hardware Requirements

The hardware components required for the project, include:
- Chassis and mechanical components
- Arduino Mega
- Basic Stamp 2
- Custom breadboard
- 2 x Continous Servo Motors
- Pulolo Reflecance Sensor
- 2 x Ultrasonic Sensors
- Parallax 2 X 16 Serial LCD With Piezo Speaker 
- Power supply
- Breadboard
- Wires
- Leds

## Software Requirements

*Transbot UI Summary*
Note: The mobile application was created using MIT App inventor

The app allows remote control and monitoring. There are 3 major phases  of the transbot_ui app. 
- CALIBRATION AND MODE SELECTION: During Calibration, the operator is able to connect app to robot via Bluetooth and select mode (Autonomous or RC mode)
- RC MODE: In RC mode, users control Transbot's movements manually using control pad. Buttons activate the delivery mechanism or return to the mode selection screen.
- AUTONOMOUS MODE: In autonomous mode,  operator input delivery coordinates, send GPS coordinates and start delivery. In case of obstacles, robot switches back to manual mode (RC mode) and enables operator navigate passed obstacle.
  
![076bc656-fd21-4937-976a-9d5b7a38c8ce_rw_1920](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/cbaa1481-6e05-4564-97fe-a9ac42375f63)
![1879ee73-cbc0-4d0a-a699-e646cd72c3c5_rw_1920](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/705b6e2b-22a2-43c7-bb55-f607a7180e32)
![last gui](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/773238b9-6b7c-4c01-aea3-851de386a004)

*Adruino Summary*

1. Arduino IDE: The Arduino Integrated Development Environment (IDE) is required to compile and upload the Arduino code to the microcontroller board.
2. Arduino Libraries:
    - QTRSensors library: Used for controlling the QTR Reflectance Sensor for line following.
    - NewPing library: Used for interfacing with the ultrasonic sensor for object detection.
    - Servo library: Used for controlling the continuous servo motors for movement.
    - SoftwareSerial library: Used for communicating with the LCD display for output indication.
    - Arduino Board Package: Ensure that the appropriate board package is installed in the Arduino IDE to support the microcontroller board you are using (e.g., Arduino Uno, Arduino Nano).
  
*Basic Stamp2 Library*

Basic Stamp2 IDE: follow link here - https://www.parallax.com/download/basic-stamp-software/



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

