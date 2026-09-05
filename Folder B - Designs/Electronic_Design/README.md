### Electronic Design and Component Justification

**Processing and Control Units**
* Primary MCU (STM32 Blue Pill): Selected for its 72MHz ARM Cortex-M3 core, which provides the necessary real-time processing speed to parse high frequency sensor data and output rapid PWM signals.

* Secondary Processor (Raspberry Pi): Implemented to run ROS2 and process camera vision algorithms. 
The Raspberry Pi handles high-level lane-heading calculations and sends directional commands to the STM32 using serial communication.

**Sensors and Navigation**
* Time-of-Flight Sensors (VL53L0X): Chosen over ultrasonic sensors (HC-SR04) for their laser based precision, millimetre-level accuracy, and faster response times which are critical for avoiding obstacles at high speeds.

* Vision and Lane-Tracking (Wide Angled Camera Module): Interfaced directly with the Raspberry Pi to feed real-time visual data into the ROS2 navigation stack. A wide angled camera lens was selected to ensure that inner and outer track boundaries remain fully visible in the frame, completely mitigating blind spots experienced by the narrow ToF sensors on wide straightaways.

* IMU (MPU6050): A 6-axis gyroscope and accelerometer used to track the vehicle's angular velocity. 
The data provided allows the MCU to detect oscillation and apply counter steering logic to help stabilize the chassis during aggressive steering.

* Boundary and Line Detection (QTR-8RC Reflectance Sensor Array): Mounted downwards at the front of the chassis to detect track lines and surface boundaries with very low latency. While the Raspberry Pi and camera provide long range predictive navigation, the QTR-8RC provides instant, high frequency, short range data to the STM32. This allows the MCU to execute high speed PID corrections without waiting for the heavier image processing overhead.
* The RC variant was selected  because its discharge time can be measured using the digital I/O pins without allowing the STM32's hardware ADC channels to be used for other telemetry.

**Power Distribution and Motor Drive**
* Power Supply (Dual 18650 Li-ion Cells): Provides 7.4V, balancing optimal energy density with sufficient mass to lower the vehicle's centre of gravity and prevent nose-diving and high-breaking conditions.

* Voltage Regulation (LM2596 Buck Converter): Steps down the raw 7.4V from the power supply down to a stable 5V line to safely power the Raspberry Pi, STM32 and logic sensors without risking thermal throttling.

* Motor Driver (TB6612FNG): Selected over the legacy L298N due to its MOSFET-based H-bridges.
It operates with higher efficiency, generates minimal waste heat and has a smaller physical footprint, creating space on the perfboard.

* Actuation and Odometry (6V GA12-N20 1500 RPM Gear Motors with Encoders): Selected to achieve a highly competitive speed. Because driving at high speeds increases the risk of traction loss, the integrated encoders are important for closed loop PID control. They provide real-time wheel RPM feedback to the STM32, ensuring that the wheels remain perfectly synchronized. This prevents spin-outs and maintains precise heading accuracy during high speed actions.

**Safety Implementation**
* Power Cutoff System: In accordance with the universal design constraints, the main battery power is routed through a primary side-mounted rocker switch and a top mounted Emergency Push Button connected in series.
This is done so that power is controlled by the rocker switch but the E-Stop button can override the rocker switch, instantly cutting off power to the circuit when necessary.



