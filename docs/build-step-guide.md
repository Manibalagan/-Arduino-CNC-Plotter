# Build Steps Guide

## Project Overview

This project focuses on the design and development of an Arduino-based XY CNC Plotter for PCB Sketching. The system is designed as a low-cost rapid prototyping platform capable of converting digital designs into physical sketches on paper or PCB surfaces. The machine combines mechanical design, embedded systems, motion control, and computer-aided manufacturing tools to create an educational and practical CNC plotting solution.

---

# 1. Project Planning and Requirement Analysis

The project was initiated to develop a compact CNC plotter capable of sketching PCB traces and simple drawings while maintaining low cost and ease of implementation. The objective was to gain practical understanding of CNC systems, G-code execution, motion control, and embedded system integration.

### Objectives

* Develop a low-cost CNC plotting system
* Achieve accurate XY positioning
* Implement G-code based motion control
* Sketch PCB layouts and vector drawings
* Learn CNC workflow from design to fabrication

---

# 2. CAD Design and 3D Modelling

The complete machine structure was first designed using CAD software. Individual parts such as the carriage assembly, pen holder, motor housing, and transmission mechanism were modeled and assembled virtually before fabrication.

### Software Used

**Fusion 360**

Website:

https://www.autodesk.com/products/fusion-360

### Design Activities

* Frame design
* Carriage design
* Pen holder design
* Integrated motor mounting design
* Motion mechanism design
* Assembly verification
* Workspace validation

The CAD stage ensured that all components fit correctly and allowed movement without interference.

---

# 3. Mechanical Assembly

After finalizing the CAD design, the machine was assembled using the fabricated structural components and 3D printed parts.

Unlike conventional CNC machines that use GT2 timing belts and pulleys, this design utilizes a custom 3D printed saw-tooth transmission mechanism to transfer motor motion into linear movement.

The motor mounting features are directly integrated into the 3D printed assembly, eliminating the need for separate mounting brackets and simplifying the overall design.

### Main Mechanical Components

* Structural frame
* Linear motion arrangement
* 3D printed saw-tooth transmission mechanism
* Integrated motor mounting structures
* Pen holder assembly
* XY carriage system

### Assembly Verification

* Smooth X-axis movement
* Smooth Y-axis movement
* Proper pen holder alignment
* Stable carriage movement
* Full workspace coverage validation

---

# 4. Electronic Hardware Integration

The control system was developed around the Arduino UNO microcontroller.

Three 28BYJ-48 stepper motors were used in the machine. Two motors are responsible for X-axis and Y-axis positioning, while the third motor controls the pen lifting mechanism.

### Hardware Components

* Arduino UNO
* 3 × 28BYJ-48 Stepper Motors
* 3 × ULN2003 Driver Boards
* 5V DC Power Adapter
* Connecting wires

### Control Architecture

Arduino UNO

↓

ULN2003 Driver Boards

↓

Stepper Motors

↓

Mechanical Motion System

The electronic system provides reliable motion control while maintaining a simple and educational hardware architecture.

---

# 5. Firmware Development

The firmware was developed using Arduino IDE and is responsible for interpreting commands and controlling machine movement.

### Software Used

**Arduino IDE**

Website:

https://www.arduino.cc/en/software

### Firmware Functions

* Stepper motor control
* XY coordinate positioning
* Pen up/down control
* Serial communication
* Motion execution
* Position tracking

The firmware acts as the bridge between the software-generated G-code and the physical machine movement.

---

# 6. Motion Control and GRBL Workflow

The CNC plotter follows a G-code based workflow for motion control.

G-code commands generated from CAD drawings are transmitted to the machine through serial communication. The machine interprets these commands and performs the required movements to reproduce the design physically.

Since the current version does not include physical limit switches, machine positioning begins from a manually defined starting location before executing a job.

### Current Positioning Method

* Manual origin setup
* Initial reference positioning
* Relative coordinate movement

### Future Improvements

Future versions of the machine may include:

* X-axis limit switch
* Y-axis limit switch
* Automatic homing
* Machine zero calibration
* Improved repeatability

These additions will enhance automation and positioning accuracy.

---

# 7. Image Processing and Vector Conversion

Images and PCB layouts must first be converted into vector paths before generating machine instructions.

### Software Used

**Inkscape**

Website:

https://inkscape.org

### Workflow

Bitmap Image

↓

Vector Trace

↓

SVG Export

### Tasks Performed

* Bitmap tracing
* Vector cleanup
* SVG generation
* Path optimization

This process converts images into machine-readable geometry.

---

# 8. Toolpath Generation and G-Code Creation

After generating SVG files, toolpaths and machine instructions are created.

### Software Used

**JSCut**

Website:

https://jscut.org

### Workflow

SVG File

↓

Toolpath Generation

↓

G-Code Export

### Outputs

* Motion paths
* CNC toolpaths
* G-code files

These files contain the movement commands executed by the CNC plotter.

---

# 9. G-Code Transmission and Machine Control

The generated G-code files are transmitted to the CNC plotter using Universal G-code Sender.

### Software Used

**Universal G-code Sender (UGS)**

Website:

https://winder.github.io/ugs_website/

### Functions

* G-code transmission
* Serial communication
* Manual machine control
* Motion testing
* Job execution

UGS acts as the communication interface between the computer and the CNC machine.

---

# 10. Machine Calibration and Testing

Calibration was performed to ensure accurate movement and reliable sketching performance.

### Calibration Activities

* Axis movement verification
* Coordinate checking
* Pen positioning adjustment
* Drawing alignment verification
* Motion repeatability testing

### Test Patterns

* Straight lines
* Squares
* Geometric shapes
* Text patterns
* PCB trace layouts

Testing confirmed the ability of the machine to reproduce digital designs with acceptable accuracy.

---

# 11. PCB Sketching Workflow

The complete workflow followed during PCB sketching is shown below:

PCB Design / Image

↓

Inkscape

(Bitmap to SVG)

↓

JSCut

(SVG to G-Code)

↓

UGS

(G-Code Transmission)

↓

Arduino UNO

(Motion Control)

↓

XY CNC Plotter

↓

PCB Sketch Output

This workflow represents the complete process from digital design creation to physical sketch generation.

---

# 12. Final Validation

The completed CNC plotter was successfully tested for drawing geometric patterns and PCB sketches.

### Achievements

* Successful XY motion control
* Reliable pen actuation
* G-code based operation
* Functional CNC plotting system
* Low-cost educational platform

The project demonstrates the integration of mechanical design, electronics, embedded programming, and computer-aided manufacturing within a single CNC platform.

---

# Software Stack Summary

| Software    | Purpose                                 |
| ----------- | --------------------------------------- |
| Fusion 360  | CAD Design and Assembly                 |
| Arduino IDE | Firmware Development                    |
| Inkscape    | Bitmap to SVG Conversion                |
| JSCut       | Toolpath and G-Code Generation          |
| UGS         | G-Code Transmission and Machine Control |

---

# Future Scope

Potential future enhancements include:

* Automatic homing system
* Limit switch integration
* Improved positioning accuracy
* Wireless control interface
* PCB drilling attachment
* Multi-tool support
* Enhanced user interface

These improvements can further increase the capability and reliability of the CNC plotting system.
