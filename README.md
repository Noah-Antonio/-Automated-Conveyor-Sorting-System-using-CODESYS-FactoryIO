# -Automated-Conveyor-Sorting-System-using-CODESYS-FactoryIO
A PLC-controlled industrial automation project that simulates an automated conveyor sorting system using **CODESYS** and **Factory I/O**. The system identifies products by type and color using a vision sensor, automatically diverts them to the appropriate sorting lane, and tracks production statistics through an integrated counting system.
## Overview
This project demonstrates the design and implementation of a PLC-based material handling system commonly found in manufacturing and distribution facilities. Objects travel along a main conveyor where they are inspected by a vision sensor. Based on the detected object type and color, PLC logic determines the appropriate destination and actuates perpendicular sorting conveyors to divert each product to its designated location.

A retroreflective sensor is used to coordinate conveyor sequencing and ensure products are sorted at the correct time. The system also provides operator controls for starting, stopping, and resetting production counts while continuously tracking the number of successfully sorted items.

## I/O List

### Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX20.0 | At Exit | Retroreflective Sensor | Detects when product exits the conveyor system |
| %IX20.1 | Start | White Pushbutton | Activates the automatic conveyor sorting system |
| %IX20.2 | Stop | Gray Pushbutton | Deactivates the automatic conveyor sorting system |
| %IX20.3 | Reset | Blue Pushbutton | Resets the product sorting counter |

### Outputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX20.0 | EntryConveyor | Conveyor Motor | Controls entry conveyor |
| %QX20.1 | StopBlade | Pneumatic Stopper | Ensures product positioning prior to sorting |
| %QX20.2 | ExitConveyor | Conveyor Motor | Controls exit conveyor |
| %QX20.3 | Sorter1Turn | Sorting Conveyor Motor | Controls product 1 diversion |
| %QX20.4 | Sorter1Belt | Conveyor Motor | Controls product 1 conveyor |
| %QX20.5 | Sorter2Turn | Sorting Conveyor Motor | Controls product 2 diversion |
| %QX20.7 | Sorter2Belt | Conveyor Motor | Controls product 2 conveyor |
| %QX20.8 | Sorter3Turn | Sorting Conveyor Motor | Controls product 3 diversion |
| %QX21.0 | Sorter3Belt | Conveyor Motor | Controls product 3 conveyor |
| %QX21.1 | StartLight | White Pilot Light | Indicates system start |
| %QX21.2 | StopLight | Gray Pilot Light | Indicates system stop |
| %QX21.3 | ResetLight | Blue Pilot Light | Indicates counter reset operation |

### Register Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Counter1 | Digital Display | Displays product 1 sorted item count |
| %QW1 | Counter2 | Digital Display | Displays product 2 sorted item count |
| %QW2 | Counter3 | Digital Display | Displays product 3 sorted item count |

### Holding Registers
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | VisionSensor | Vision Sensor | Detects and temporarily stores product color and type |

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
- CODESYS
- Factory I/O
- Modbus TCP/IP
- IEC 61131-3 Ladder Diagram (LD)
  
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
