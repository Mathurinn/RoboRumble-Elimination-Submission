# Robo Rumble 2026: Elimination Round Submission
**Category:** Robo Grand Prix (Autonomous Racing)
**Team:** Team Apex (Mathurin Moundzika-Kibamba and Ayanda Tshabangu)

## Project Summary
This repository contains the complete engineering, design, and software architecture for APEX-1, a fully autonomous racing robot for the Robo Grand Prix category. Per the universal design constraints, the physical vehicle is designed to weigh under 5 kg and fit within a 50 cm x 50 cm footprint.

To adhere strictly to the category rules, the vehicle is 100% autonomous with no remote control or human intervention. Initial prototype testing evaluated Time-of-Flight (ToF) sensors for wall following. Based on simulation data, the final electronic architecture justifies a transition to a lightweight, custom OpenCV camera vision system integrated with an STM32 microcontroller to ensure accurate lane heading on wide track segments. The physical build features a mandatory external ON/OFF switch and an integrated Emergency Stop (E-Stop) mechanism.

## Repository Directory Map

### 📁 [Folder A: Source Code](./Folder%20A%20-%20Source%20Code)
Contains the software architecture and logic used to drive the robot autonomously.
* **Firmware:** Microcontroller code (C++/STM32) for sensor parsing, state-machine execution, and motor PID control.
* **Vision Pipeline:** Standalone OpenCV Python/C++ scripts for lane extraction and track severity calculations.
* **Flowcharts:** Visual logic trees mapping the autonomous decision-making loops.

### 📁 [Folder B: Designs](./Folder%20B%20-%20Designs)
Contains the physical blueprints, circuit diagrams, and simulation validation required for fabrication.
* **Mechanical_Design:** CAD models and `Mechanical_Assembly.md` demonstrating chassis fabrication, 25% gyroid infill justification, and mass distribution (711g).
* **Electronic_Design:** Proteus/KiCad schematics and `Circuit_Architecture.md` detailing the STM32 integration, motor drivers, and the mandatory, annotated Emergency Stop (E-Stop) safety circuit.
* **Simulation:** Video evidence (via Google Drive), Wokwi logic testing, and kinematic data validating the mechanical turning radius prior to physical assembly.

### 📁 [Folder C: Documentation](./Folder%20C%20-%20Documentation)
Contains the core project management, financial breakdowns, and technical reports.
* **Pitch_Deck.pdf:** A 7-slide presentation covering the problem statement, solution, buildability, final costs, and team roles.
* **Bill_of_Materials.xlsx:** A comprehensive component breakdown including supplier URLs, quantities, unit costs, and the final total cost highlighted in RED.
* **Holistic_Build_Document.pdf:** The master technical report detailing category constraints, mechanical/electronic justifications, and the pivot from ToF sensing to OpenCV camera vision based on simulation data.
* **FQA_Attendance_Log.md:** Verified attendance records and screenshots from the facilitator Q&A sessions.
