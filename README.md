# Automated Conveyor Sorting System
A PLC-controlled material handling system developed using **CODESYS** and **Factory I/O**. The system classifies products using a vision sensor, automatically routes items using sorting conveyors, and tracks production counts through integrated PLC logic.
## Overview
This project demonstrates the design and implementation of a PLC-based material handling system commonly found in manufacturing and distribution facilities. Objects travel along a main conveyor where they are inspected by a vision sensor. Based on the detected object type and color, PLC logic determines the appropriate destination and actuates perpendicular sorting conveyors to divert each product to its designated location.

A retroreflective sensor is used to coordinate conveyor sequencing and ensure products are sorted at the correct time. The system also provides operator controls for starting, stopping, and resetting production counts while continuously tracking the number of successfully sorted items.



## Features
- PLC ladder logic developed in CODESYS
- 3D industrial simulation using Factory I/O
- Vision-based object classification by type and color
- Retroreflective sensor for conveyor sequencing
- Automated product sorting using perpendicular conveyor belts
- Timer-based sequencing for reliable material handling
- Item counting with reset functionality
- Start and stop operator controls
- Fully simulated industrial automation cell


  
## Technologies
- **CODESYS**
- **Factory I/O**
- **Modbus TCP/IP Communication**
- **IEC 61131-3 Ladder Diagram (LD)**


  
## Engineering Concepts Demonstrated
- PLC Programming
- Industrial Automation
- Ladder Logic
- Sensor Integration
- Motor Control
- Timer and Counter Instructions
- Sequential Control
- Material Handling Systems
- Industrial I/O Mapping
- Automation System Testing and Validation
- Industrial Sensor Integration
- Machine Sequencing

  
## I/O List

### Digital Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX20.0 | Product_Exit_Sensor | Retroreflective Sensor | Detects when product exits the conveyor system |
| %IX20.1 | Start_CMD | White Pushbutton | Activates automatic conveyor sorting operation |
| %IX20.2 | Stop_CMD | Gray Pushbutton | Stops automatic conveyor sorting operation |
| %IX20.3 | Reset_Count_CMD | Blue Pushbutton | Resets product sorting counter values |
| %IX20.4 | Emergency_Stop_CMD | Emergency Stop Button | Immediately stops all system motion and disables outputs |
| %IX20.5 | Emergency_Reset_CMD | Red Pushbutton | Resets emergency stop condition after fault is cleared |

### Digital Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX20.0 | Entry_Conveyor_CMD | Conveyor Motor | Controls entry conveyor operation |
| %QX20.1 | Product_Stopper_CMD | Pneumatic Stopper | Positions product prior to sorting |
| %QX20.2 | Exit_Conveyor_CMD | Conveyor Motor | Controls exit conveyor operation |
| %QX20.3 | Sorter1_Turn_CMD | Sorting Conveyor Motor | Diverts product type 1 to sorting lane |
| %QX20.4 | Sorter1_Belt_CMD | Conveyor Motor | Controls product type 1 conveyor |
| %QX20.5 | Sorter2_Turn_CMD | Sorting Conveyor Motor | Diverts product type 2 to sorting lane |
| %QX20.7 | Sorter2_Belt_CMD | Conveyor Motor | Controls product type 2 conveyor |
| %QX20.8 | Sorter3_Turn_CMD | Sorting Conveyor Motor | Diverts product type 3 to sorting lane |
| %QX21.0 | Sorter3_Belt_CMD | Conveyor Motor | Controls product type 3 conveyor |
| %QX21.1 | Start_Status_Light | White Pilot Light | Indicates system start status |
| %QX21.2 | Stop_Status_Light | Gray Pilot Light | Indicates system stop status |
| %QX21.3 | Reset_Count_Status_Light | Blue Pilot Light | Indicates counter reset operation |
| %QX21.4 | Emergency_Status_Light | Red Pilot Light | Indicates emergency stop condition is active |

### Register Inputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | Vision_Sensor_Data | Vision Sensor | Provides product classification data based on type and color |

### Register Outputs

| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Product1_Count_Display | Digital Display | Displays sorted item count for product type 1 |
| %QW1 | Product2_Count_Display | Digital Display | Displays sorted item count for product type 2 |
| %QW2 | Product3_Count_Display | Digital Display | Displays sorted item count for product type 3 |



## Demonstration
https://youtu.be/R_T0u_bhNYo

