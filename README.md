# Lab Assignment: GPIO Control and PYNQ-Z2 Exploration

**Author**: Matthew Gomogda  
**Email**: matthewgomogda@gmail.com  
**Student Email**: mgomogda@ucsd.edu  

---

## Overview

This lab assignment focuses on exploring the GPIO functionality of the PYNQ-Z2 board by utilizing the programmable logic (PL) and processing system (PS). The primary goals include understanding how the PL manages peripherals like LEDs, buttons, switches, and PMOD headers, and how some peripherals are directly controlled by the PS. The assignment also emphasizes interfacing with GPIO pins for sending and receiving data through MicroBlaze soft processors and Python.

---

## Objectives

1. **GPIO Manipulation**: 
   - Learn to control GPIO pins for output (e.g., LEDs) and input (e.g., buttons) using both MicroBlaze C code and Python.
   - Understand how to send and receive data over GPIO using bit-level control.

2. **PL and PS Roles**: 
   - Differentiate between the responsibilities of the PL (peripheral control) and PS (communication protocols like UART, SPI, and I2C).

3. **Interfacing PMODs**: 
   - Explore PMOD header control for hardware communication.

4. **Custom Code**: 
   - Develop and test code for sending 2-bit data using GPIO and verifying the data flow between connected pins.

---

## Key Learnings

- The PL primarily controls peripherals like LEDs, buttons, switches, and PMOD headers, while the PS handles high-level communication protocols.
- GPIO operations, such as reading and writing pin values, can be implemented both in MicroBlaze C code and Python.
- The PYNQ-Z2 board provides a unique blend of FPGA configurability and ARM-based processing, allowing for efficient peripheral management.

---

## Issues Encountered

One aspect that remains unclear is the precise communication mechanism between the PS and PL, particularly how the AXI interface facilitates data transfer. This understanding is crucial for designing more efficient systems using the PYNQ platform.

---

## How to Run the Code

1. **MicroBlaze C Code**:
   - Use the `%%microblaze` magic command to execute low-level C code on the MicroBlaze processor for GPIO operations.
   - Ensure the `base` overlay is loaded before running any MicroBlaze code.

2. **Python Code**:
   - Load the `base` overlay using:
     ```python
     from pynq.overlays.base import BaseOverlay
     base = BaseOverlay("base.bit")
     ```
   - Use Python scripts to control GPIO for higher-level tasks like sending and receiving 2-bit data.

3. **Hardware Setup**:
   - Connect GPIO pins as required (e.g., Pin 0 to Pin 2, Pin 1 to Pin 3) to test data flow between sending and receiving pins.

---

## Contact
For questions or feedback, feel free to contact me at:

- **Personal Email**: [matthewgomogda@gmail.com](mailto:matthewgomogda@gmail.com)
- **Student Email**: [mgomogda@ucsd.edu](mailto:mgomogda@ucsd.edu)

---
