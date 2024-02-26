# Transbot_1.0

To learn more about this robotics project, look into the presentation file. You can find both arduino and basic stamp codes in the files named arduino_interface_code and basic_stamp_interface_code respectively.


# Requirements

An Arduino Nano was used for this project and you can open the arduino code using the arduino IDE.
Also the Basic stamp2 micro controller was used as the main connector for sensors. To open the basic stamp code, you need to download the basic stamp editor software here https://www.parallax.com/download/basic-stamp-software/



# Autonomous Parking Vehicle (AGV)

This project involves using an Arduino UNO microcontroller to create a parking lot robot capable of autonomously navigating and parking in the nearest available spot. By combining line following, ultrasonic sensing, and a search algorithm, the robot identifies and parks in the nearest open parking space, validated through extensive testing.

# Parking Lot Layout
![parking_lot_layout](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/896fe77e-4570-4bf2-bc5a-13d0423bf5ed)

# Robot Demo
![Untitled video - Made with Clipchamp (6)](https://github.com/IJAMUL1/Automated-Factory-Guided-Vehicle/assets/60096099/e307b82f-e207-4fdd-a5fa-0d75c333c798)

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

