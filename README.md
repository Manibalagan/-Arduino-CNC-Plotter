# XY CNC Plotter for PCB Sketching

## Introduction

The XY CNC Plotter for PCB Sketching is a low-cost computer-controlled machine developed to automate the process of drawing PCB layouts. The system utilizes an Arduino UNO as the central controller and employs stepper motors to achieve precise movement along the X and Y axes. By converting digital PCB designs into motion commands, the machine can reproduce circuit traces directly on PCB substrates, significantly reducing the time required for prototype development.

## Project Motivation

Traditional PCB fabrication methods often require external manufacturing services, resulting in delays of several days and increased prototyping costs. During product development and academic projects, multiple design iterations are usually necessary before achieving a successful circuit design. Waiting for fabrication during each iteration slows down the development cycle considerably. This project was developed to provide a rapid, affordable, and educational solution that allows PCB designs to be physically sketched within minutes.

## System Overview

The plotter operates using a Cartesian coordinate system where independent stepper motors control movement along the X-axis and Y-axis. A pen mechanism mounted on the moving carriage is responsible for drawing PCB traces. The Arduino controller interprets motion commands and generates the required control signals for the motor driver circuits. Through coordinated movement of both axes, complex PCB layouts can be reproduced accurately on the drawing surface.

## Mechanical Design

The mechanical structure consists of a rigid frame, linear motion guides, timing belt transmission mechanisms, and custom mounting components. GT2 timing belts are used to transfer motor motion to the moving carriage while maintaining positional accuracy. The frame is designed to provide adequate stiffness while remaining lightweight and cost-effective. The compact structure ensures smooth motion and minimizes vibration during operation.

## Electronic Design

The electronic control system is built around the Arduino UNO microcontroller. Three 28BYJ-48 stepper motors are employed for axis control and pen actuation. ULN2003 driver boards interface the motors with the microcontroller and provide sufficient current amplification for reliable operation. Limit switches are incorporated to establish reference positions and improve repeatability. A regulated power supply provides stable power to all electronic components.

## Motion Control and Firmware

The firmware is responsible for interpreting movement commands, calculating motor positions, and generating step sequences for the motors. Motion control is implemented using coordinate-based positioning techniques that allow precise movement along both axes simultaneously. The software also manages pen-up and pen-down operations, enabling the machine to draw complex geometries and PCB traces with high accuracy.

## Performance

The developed system achieves a practical positioning resolution of approximately 0.05 mm and an overall accuracy of ±0.2 mm. Drawing speeds between 200 mm/min and 400 mm/min provide a balance between speed and trace quality. The machine is capable of producing PCB sketches suitable for educational activities, circuit verification, and rapid prototyping applications.

## Applications

The CNC plotter can be used for PCB sketching, educational demonstrations, CNC programming experiments, coordinate system studies, motion control research, and rapid prototype development. The project also serves as an effective learning platform for understanding the integration of mechanical systems, electronics, embedded programming, and automation.

## Conclusion

The XY CNC Plotter successfully demonstrates how low-cost components and systematic engineering design can be combined to create a practical rapid prototyping platform. The project provides valuable experience in CNC technology, embedded systems, motion control, and mechatronic system integration while offering a cost-effective alternative for educational PCB prototyping.
