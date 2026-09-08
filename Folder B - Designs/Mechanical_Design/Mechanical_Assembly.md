### Mechanical Design

**Chassis Architecture & 3D Printing**
The vehicle uses a custom-designed, two piece chassis (base tub and top lid) which is fabricated using 3D printing. The shell is printed using a tri-hexagonal infill pattern which provides a better strength-to-weight density compared to standard grid infills. This helps balance structural integrity and economic feasibility. The chassis density is reduced to 15% to keep the chassis economically viable while maintaining a low chance of chipping. Localized areas supporting the hardware components are printed at a density of 20-25% to ensure that the threads and pillars are able to withstand mechanical stress and maintain a stable centre of gravity.
<img width="982" height="766" alt="Screenshot 2026-09-05 193945" src="https://github.com/user-attachments/assets/44898105-20d2-4f5d-9a1e-de652634428d" />


**Drive System and Kinematics**
The robot makes use of a differential drive system that uses two GA12-N20 DC gear motors. These motors are fastened to the chassis using dedicated gear mounts and screws with locking nuts. Traction is provided by 43mm diameter wheels that fit directly onto the D-shafts of the gear motors. A rear mounted castor ball wheel is secured directly through the underside of the chassis with locking nuts. This helps to establish a stable, 3-point turning radius that helps ground the weight of the chassis.
<img width="981" height="767" alt="Screenshot 2026-09-05 194927" src="https://github.com/user-attachments/assets/1d3ed840-1c96-4d3c-9fb3-edb0c8a43db2" />



**Component Fastening and Electronic Integration**
The internal electronics of the robot are designed for modularity and vibration resistance. The primary modules and microcontrollers such as the STM32 Blue Pill, LM2596 buck converter and motor driver, are not permanently soldered into the perfboard. They are placed into female header pins which are soldered onto the perfboard. The perfboard is screwed securely into structural pillars that are integrated into the chassis tub. The secondary processor, the Raspberry pi, is screwed into four pillars on the underside of the lid to isolate it from motor vibration and to create more space inside the tub of the chassis. The Raspberry Pi Camera module is placed in a adjustable mount that is fused with the top lid of the chassis.
<img width="983" height="765" alt="image" src="https://github.com/user-attachments/assets/f2223a6f-bef3-4aec-b8c8-e7fe35ace20e" />
<img width="983" height="761" alt="image" src="https://github.com/user-attachments/assets/fe2f208d-77b7-4dfc-be10-b71e98c015e9" />

**Safety Mechanisms and Sensor Placement**
The physical chassis incorporates dedicated housing for power cutoff systems in accordance with the competition's safety constraints. A primary rocker switch is fitted through a measured cutout in the side wall of the chassis, while the mandatory E-Stop (Emergency Stop) is mounted on the top of the lid for easier, immediate external access. For autonomous navigation, two ToF sensors are fitted into the front of the chassis at outward 45 degree angles to assist with cornering predictions. The top lid acts as a back support brace for these sensors ensuring that they remain perfectly aligned in the case of high-speed collisions. The QTR-8RC is placed under the vehicle at a height that is optimal for operation and is bolted onto the inside of the chassis.
<img width="990" height="765" alt="image" src="https://github.com/user-attachments/assets/6e5f3f80-5a9c-4744-873c-6fe83a4f3bc0" />
<img width="992" height="763" alt="image" src="https://github.com/user-attachments/assets/79937259-d06d-45b2-b969-87d733456ffc" />



