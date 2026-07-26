# -Automated-Conveyor-Sorting-System-using-CODESYS-FactoryIO
A PLC-controlled industrial automation project that simulates an automated conveyor sorting system using **CODESYS** and **Factory I/O**. The system identifies products by type and color using a vision sensor, automatically diverts them to the appropriate sorting lane, and tracks production statistics through an integrated counting system.
## Overview
This project demonstrates the design and implementation of a PLC-based material handling system commonly found in manufacturing and distribution facilities. Objects travel along a main conveyor where they are inspected by a vision sensor. Based on the detected object type and color, PLC logic determines the appropriate destination and actuates perpendicular sorting conveyors to divert each product to its designated location.

A retroreflective sensor is used to coordinate conveyor sequencing and ensure products are sorted at the correct time. The system also provides operator controls for starting, stopping, and resetting production counts while continuously tracking the number of successfully sorted items.

## I/O List

### Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IX20.0 | At Exit | Retroreflective Sensor | Detects When Product Leaves Conveyor System to be Extracted |
| %IX20.1 | Start | White PushButton | Activates the Automatic Conveyor Sorting System |
| %IX20.2 | Stop | Gray PushButton | Deactivates the Automatic Conveyor Sorting System |
| %IX20.3 | Reset | Blue PushButton | Resets the Product Sorted Item Count |

### Outputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QX20.0 | EntryConveyor | Conveyor Motor | Controls Entry Conveyor |
| %QX20.1 | StopBlade | Pneumatic Stopper | Ensures Product Positioning Prior to Sorting |
| %QX20.2 | ExitConveyor | Conveyor Motor | Controls Exit Conveyor |
| %QX20.3 | Sorter1Turn | Sorting Conveyor Motor | Controls Product 1 Diversion |
| %QX20.4 | Sorter1Belt | Conveyor Motor | Controls Product 1 Conveyor |
| %QX20.5 | Sorter2Turn | Sorting Conveyor Motor | Controls Product 2 Diversion |
| %QX20.7 | Sorter2Belt | Conveyor Motor | Controls Product 2 Conveyor |
| %QX20.8 | Sorter3Turn | Sorting Conveyor Motor | Controls Product 3 Diversion |
| %QX21.0 | Sorter3Belt | Conveyor Motor | Controls Product 3 Conveyor |
| %QX21.1 | StartLight | White Pilot Light | Indicates System Start |
| %QX21.2 | StopLight | Gray Pilot Light | Indicates System Stop |
| %QX21.3 | ResetLight | Blue Pilot Light | Indicates Counter Reset |

### Register Inputs
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %QW0 | Counter1 | Digital Display | Displays Product 1 Sorted Item Count |
| %QW1 | Counter2 | Digital Display | Displays Product 2 Sorted Item Count |
| %QW2 | Counter3 | Digital Display | Displays Product 3 Sorted Item Count |

### Holding Registers
| Address | Tag | Device | Description |
|---------|-----|--------|-------------|
| %IW0 | VisionSensor | Vision Sensor | Detects and Temporarily Stores Product Color/Type |

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
