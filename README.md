## -Automated-Conveyor-Sorting-System-using-CODESYS-FactoryIO
A PLC-controlled industrial automation project that simulates an automated conveyor sorting system using **CODESYS** and **Factory I/O**. The system identifies products by type and color using a vision sensor, automatically diverts them to the appropriate sorting lane, and tracks production statistics through an integrated counting system.
# Overview
This project demonstrates the design and implementation of a PLC-based material handling system commonly found in manufacturing and distribution facilities. Objects travel along a main conveyor where they are inspected by a vision sensor. Based on the detected object type and color, PLC logic determines the appropriate destination and actuates perpendicular sorting conveyors to divert each product to its designated location.

A retroreflective sensor is used to coordinate conveyor sequencing and ensure products are sorted at the correct time. The system also provides operator controls for starting, stopping, and resetting production counts while continuously tracking the number of successfully sorted items.
# Features
- PLC ladder logic developed in CODESYS
- 3D industrial simulation using Factory I/O
- Vision-based object classification by type and color
- Retroreflective sensor for conveyor sequencing
- Automated product sorting using perpendicular conveyor belts
- Timer-based sequencing for reliable material handling
- Item counting with reset functionality
- Start and stop operator controls
- Fully simulated industrial automation cell
# Technologies
- CODESYS
- Factory I/O
- IEC 61131-3 Ladder Logic
# Engineering Concepts Demonstrated
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
