# Robo Rumble 2026: Elimination Round Submission
**Category:** Robo Grand Prix (Autonomous Racing)
**Team:** Team Apex (Mathurin Moundzika-Kibamba and Ayanda Tshabangu)

## Project Summary
This repository contains the complete engineering, design, and software architecture for APEX-1, a fully autonomous racing robot for the Robo Grand Prix category. Per the universal design constraints, the physical vehicle is designed to weigh under 5 kg and fit within a 50 cm x 50 cm footprint.

To adhere strictly to the category rules, the vehicle is 100% autonomous with no remote control or human intervention. Initial prototype testing evaluated Time-of-Flight (ToF) sensors for wall following. Based on simulation data, the final electronic architecture justifies a transition to a lightweight, custom OpenCV camera vision system integrated with an STM32 microcontroller to ensure accurate lane heading on wide track segments. The physical build features a mandatory external ON/OFF switch and an integrated Emergency Stop (E-Stop) mechanism.

### Repository Directory Map

**📁 Folder A: Source Code**

Contains the software architecture, flowcharts, and logic used to drive the robot autonomously.

* **APEX_ONE_Source_Code.pdf:** The complete C++ firmware codebase for sensor parsing, state-machine execution, and motor PID control.
* **Computer_Programming_And_Control.pdf:** The required technical statement detailing our programming methods, dual-core framework, and Wokwi simulation constraints.
* **APEX_ONE_Flowchart.jpeg:** Visual logic tree mapping the autonomous decision-making loops and failsafe conditions.

**📁 Folder B: Designs**

Contains the physical blueprints, circuit diagrams, and simulation validation required for fabrication.

* **Mechanical_Design:** Contains the raw CAD assembly files (`APEX1.zip`) and `APEX_ONE_Mechanical Design.pdf` demonstrating chassis fabrication, 25% gyroid infill justification, and mass distribution (711g).
* **Electronic_Design:** Contains `APEX_ONE_Electronic_Design.pdf` detailing the STM32 integration, power distribution, and component justification.
* **Schematics:** Hosts the raw CAD Proteus project file (`.pdsprj`) and high-resolution annotated screenshots of the circuitry, explicitly showing the mandatory E-Stop mechanism and Wokwi logic map.
* **Simulation:** Contains `APEX_ONE_Simulation.pdf`, featuring video evidence links (via Google Drive) and kinematic data validating the mechanical turning radius prior to physical assembly.

**📁 Folder C: Documentation**

Contains the core project management, financial breakdowns, and master technical reports.

* **Apex_One_Pitch_Deck.pdf:** A presentation covering the problem statement, solution, buildability, final costs, and team roles.
* **Bill_of_Materials.xlsx:** A comprehensive component breakdown including supplier URLs, quantities, unit costs, and the final total cost highlighted in RED.
* **APEX_1_Holistic_Build_Document.pdf:** The master technical report detailing category constraints, mechanical/electronic justifications, and the pivot from ToF sensing to OpenCV camera vision based on simulation data.
* **FQA_Attendance_Log.md & FQA_Proof:** Verified attendance records and screenshot evidence from the facilitator Q&A sessions.
