BCM CAN Test Project
1. Project Overview
This project is a CAN-based test automation framework for Body Control Module (BCM) light functions, developed using Python, Kvaser CAN interface, and DBC-based signal decoding.
The project focuses on validating BCM_Light_Status CAN messages, including:
Turn Left Indicator
Turn Right Indicator
Hazard Light
The test framework is designed to simulate real automotive test workflows commonly used in HIL

2. System Architecture
+------------------+
|   Test Case      |
| bcm_light_test   |
+--------+---------+
         |
         v
+------------------+        +------------------+
|  Python Test     |  CAN   |     BCM ECU /    |
|  Framework       +------->|   CAN Simulator  |
+--------+---------+        +------------------+
         |
         v
+------------------+
| Kvaser Interface |
+------------------+

3.Software & Tools
- Kvaser CanKing – CAN message transmission and logging  
- Python – test automation and result validation  
- Kvaser Database Editor – CAN message & signal definition
- Busmaster - Performed CAN-based testing

4. Skills Demonstrated
CAN protocol fundamentals
Automotive DBC analysis
Python-based test automation
Kvaser CAN hardware integration
TX/RX validation and signal-level checking

5. Video Demo
https://drive.google.com/drive/folders/112-AWgRLEbG9Pjxc9rcmz0YYQRTutPv2

6. DBC File: 
https://drive.google.com/drive/folders/1q-dMScXx5xf38_MUVTgqfMGmDP9lQ8ZJ?usp=sharing
BO_ 256 BCM_Status: 8 BCM
 SG_ Door_FL : 0|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway
 SG_ Door_FR : 1|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway
 SG_ Door_RL : 2|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway
 SG_ Door_RR : 3|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway

BO_ 513 BCM_Light_Status: 8 BCM
 SG_ TurnLeft : 0|1@1+ (1,0) [0|1] ""  Gateway,Instrumentcluster
 SG_ TurnRight : 1|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway
 SG_ Hazard : 2|1@1+ (1,0) [0|1] ""  Instrumentcluster,Gateway