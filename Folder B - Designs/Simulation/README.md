### Simulation Testing & Sensor Limitation Discovery

**Kinematic Validation (Unity Physics Engine)**
Initial autonomous testing was conducted in Unity using dual Time-of-Flight (TOF) distance sensors for corridor centering. The simulation successfully validated the mechanical chassis design, demonstrating that the lowered center of mass provides a stable turning radius through tight chicanes without tipping or nose-diving at 1.5 m/s.

https://drive.google.com/drive/folders/1x00z_MCNwTP476MxUhtKEg-Wvh_yydqd?usp=drive_link

**Electronic Justification Pivot**
While the chassis proved stable, the simulation data revealed a critical flaw in purely TOF-based navigation: on track straights wider than 2.5 meters, the sensors lose simultaneous wall contact. Without lane-heading awareness, the vehicle suffers from oscillation and diagonal drifting. 

This simulated failure provided the exact data needed to finalize our electronic architecture. To prevent drifting in the physical Robo Grand Prix, we are upgrading from purely TOF-based logic to a camera-vision system utilizing ROS2 obstacle avoidance algorithms, ensuring the physical bot tracks the painted lanes rather than relying on physical walls.

**State-Machine Validation (Wokwi Logic Simulation)**
To validate the upgraded control architecture, the core C++ navigation state-machine and I2C sensor parsing logic were simulated using Wokwi. This confirmed that our STM32 microcontroller can successfully integrate real-time telemetry from the IMU, INA219 current sensor, and wheel encoders while executing our PID steering algorithms.

[Insert Link to Wokwi Simulation Project Here]
