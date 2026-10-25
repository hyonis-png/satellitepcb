IMU & Magnetometer PCB

A custom PCB designed in KiCad to integrate an IMU (Inertial Measurement Unit) and a magnetometer for a university satellite design project.

The board was designed to collect acceleration, angular velocity, and magnetic field measurements through an I²C interface, allowing an external microcontroller to retrieve sensor data.

Project Status: PCB design completed. ERC and DRC passed. The board has not been manufactured or physically tested.

Overview

The goal of this project was to design a compact sensor board capable of interfacing with a satellite's onboard electronics.

The board integrates two sensors:

ICM-42688-P: A 6-axis IMU containing a 3-axis accelerometer and 3-axis gyroscope.
LIS2MDL: A 3-axis magnetometer used to measure magnetic fields.

Both sensors communicate over I²C, allowing them to share the same communication bus.

Hardware Components
Component	Description
ICM-42688-P	6-axis IMU
LIS2MDL	3-axis magnetometer
4.7 kΩ resistors	I²C pull-up resistors
Decoupling capacitors	Power supply filtering
4-pin connector	External power and I²C interface
Mounting holes	Mechanical integration

The board is designed to operate from a 3.3 V supply.

Design Process
1. Schematic Design

The schematic was developed in KiCad using the manufacturers' datasheets as references.

The main considerations included:

Identifying the required power and communication pins.
Configuring both sensors for I²C communication.
Adding pull-up resistors to the SDA and SCL lines.
Adding decoupling capacitors for power supply stability.
Connecting both sensors to a common 3.3 V supply and ground.

KiCad's Electrical Rules Checker (ERC) was used to verify the schematic.

2. PCB Layout

After completing the schematic, the components were assigned footprints and transferred to KiCad's PCB editor.

The layout includes:

Copper traces connecting the sensors and supporting components.
A ground copper pour.
A 4-pin connector for interfacing with external electronics.
Four mounting holes for mechanical installation.

Component placement and routing were completed with consideration for signal integrity, power distribution, and board integration.

3. Design Verification

The design was checked using KiCad's built-in verification tools.

Check	Status
Electrical Rules Check (ERC)	Passed
Design Rules Check (DRC)	Passed
PCB manufacturing	Not completed
Hardware validation	Not completed

Passing ERC and DRC confirms that the design satisfies the configured electrical and layout rules. It does not guarantee that the hardware will function correctly.

Potential Improvements

Although the PCB design was completed, several improvements could be made before manufacturing:

Optimize component placement and trace routing.
Improve silkscreen readability.
Review magnetometer placement to minimize magnetic interference.
Verify component footprints and datasheet-specific layout recommendations.
Manufacture and test the PCB.
Validate I²C communication and sensor readings using a microcontroller.
Applications

Although originally designed for a satellite project, the same hardware and design process can be applied to:

Drone navigation and orientation sensing.
Robotics and motion tracking.
Embedded sensor systems.
Aerospace electronics.
Tools Used
KiCad — Schematic capture and PCB layout.
Component datasheets — Electrical specifications, pin configurations, and design requirements.
KiCad ERC/DRC — Electrical and PCB layout verification.
Project Status

This project represents the design and verification stage of PCB development.

The schematic and PCB layout were completed, but the board was not manufactured due to the project's development timeline.

Future work would involve reviewing the design for manufacturing, ordering the PCB, assembling the components, and validating sensor communication and measurements.<img width="927" height="462" alt="image" src="https://github.com/user-attachments/assets/88ec3cc9-c28f-40a2-aa38-b6dec2a557f4" />
<img width="1128" height="577" alt="image" src="https://github.com/user-attachments/assets/7a0d9e11-75dd-4ddb-9a3d-6f35b2907ffe" />
