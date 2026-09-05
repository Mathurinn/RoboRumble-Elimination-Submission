# Robo Rumble 2026: Elimination Round Submission
**Category:** Robo Grand Prix (Autonomous Racing)
**Team/Competitor:** Mathurin Nimrod Moundzika-Kibamba

## High-Level Project Summary
This repository contains the complete engineering, design, and software architecture for a fully autonomous racing robot built for the Robo Grand Prix category. Per the universal design constraints, the physical vehicle is designed to weigh under 5 kg and fit within a 50 cm x 50 cm footprint[cite: 1]. 

To adhere strictly to the category rules, the vehicle is 100% autonomous with no remote control or human intervention[cite: 1]. The initial prototype design evaluated Time-of-Flight (TOF) sensor algorithms for wall-following in a Unity physics simulation. Based on the simulation data, the final electronic architecture justifies a transition to a camera-based ROS2 vision system integrated with an STM32 microcontroller to ensure accurate lane-heading on wide track segments. The physical build features a mandatory external ON/OFF switch and an integrated Emergency Stop (E-Stop) mechanism[cite: 1].

## Repository Directory Map

### 📁 [Folder A: Source Code](./Folder%20A%20-%20Source%20Code)
Contains the software architecture and logic used to drive the robot autonomously[cite: 1].
* **`Firmware/`**: Microcontroller code (C/C++) for sensor parsing and motor control.
* **`Flowcharts/`**: Visual logic trees mapping the autonomous decision-making loops and state machines[cite: 1].

### 📁 [Folder B: Designs](./Folder%20B%20-%20Designs)
Contains the physical blueprints, circuit diagrams, and simulation validation required for fabrication[cite: 1].
* **`Mechanical_Design/`**: CAD models and renders demonstrating chassis fabrication, component fastening, and weight distribution[cite: 1].
* **`Electronic_Design/`**: Circuit schematics detailing the STM32 integration, motor drivers, and the mandatory, annotated Emergency Stop (E-Stop) safety circuit[cite: 1].
* **`Simulation/`**: Video evidence, mock IMU telemetry logs, and kinematic testing data validating the mechanical turning radius and sensor limitations prior to physical assembly[cite: 1].

### 📁 [Folder C: Documentation](./Folder%20C%20-%20Documentation)
Contains the core project management, financial breakdowns, and technical reports[cite: 1].
* **`Pitch_Deck.pdf`**: A 7-slide presentation covering the problem statement, solution, marketability, final costs, and team roles[cite: 1].
* **`Bill_of_Materials.xlsx`**: A comprehensive component breakdown including supplier URLs, quantities, unit costs, and the final total cost highlighted in RED[cite: 1].
* **`Holistic_Build_Document.pdf`**: The master technical report detailing category constraints, mechanical/electronic justifications, and the pivot from TOF sensing to ROS2 camera vision based on simulation data[cite: 1].
* **`FQA_Attendance_Log.md`**: Verified attendance records and screenshots from the Facilitator Q&A sessions[cite: 1].
