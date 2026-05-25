# 32-bit-5-Stages-Pipelined-MIPS-Processor-on-FPGA
FPGA-based 32-bit 5-stage pipelined MIPS processor implemented using Verilog HDL on the Basys 3 Artix-7 FPGA board. The processor supports arithmetic operations, hazard handling, dot-product computation, and 2×2 matrix multiplication with real-time output visualization using seven-segment displays.

---

# Project Overview

This project implements a complete 32-bit pipelined MIPS processor architecture using Verilog HDL. The processor follows a five-stage pipeline architecture:

1. Instruction Fetch (IF)
2. Instruction Decode (ID)
3. Execute (EX)
4. Memory Access (MEM)
5. Write Back (WB)

The architecture integrates forwarding and flush control mechanisms to reduce pipeline hazards and improve instruction throughput.

---

# Features

- 32-bit MIPS Architecture
- 5-Stage Pipeline
- Verilog HDL Design
- FPGA Implementation on Basys 3
- Hazard Detection and Handling
- Forwarding Unit
- Flush Control Unit
- Arithmetic Operations
- Dot Product Computation
- 2×2 Matrix Multiplication
- Seven Segment Display Output
- Switch-Based Mode Selection
- Xilinx Vivado Compatible

---

# Pipeline Stages

| Stage | Description |
|------|-------------|
| IF | Instruction Fetch |
| ID | Instruction Decode |
| EX | Execute |
| MEM | Memory Access |
| WB | Write Back |

---

# Major Modules

- Program Counter (PC)
- Instruction Memory
- Register File
- ALU
- ALU Control Unit
- Main Control Unit
- Data Memory
- Pipeline Registers
- Forwarding Unit
- Flush Control Unit
- Seven Segment Display Driver

---

# Supported Operations

| Operation | Description |
|----------|-------------|
| ADD | Addition |
| SUB | Subtraction |
| MUL | Multiplication |
| DOT | Dot Product |
| MATMUL | 2×2 Matrix Multiplication |

---

# FPGA Board

- Basys 3 FPGA Board
- Xilinx Artix-7 FPGA

---

# Tools Used

- Verilog HDL
- Xilinx Vivado Design Suite
- Basys 3 FPGA Board

---

# Simulation

The processor was verified using:
- Behavioral Simulation
- RTL Schematic Verification
- FPGA Hardware Testing

---

# FPGA Output

Results are displayed on:
- Seven Segment Display
- FPGA LEDs
- Switch-Controlled Operation Modes

---

# Switch Configuration

| Switch Mode | Operation |
|-------------|-----------|
| 00 | 2×2 Matrix Multiplication |
| 01 | Dot Product |
| 10 | Addition |
| 11 | Subtraction |

---

# Project Structure


```bash
MIPS-X/
│
├── src/
│   ├── MIPSpipeline.v
│   ├── alu.v
│   ├── controlUnit.v
│   ├── instructionMem.v
│   ├── dataMem.v
│   ├── forwardingUnit.v
│   ├── flush_block.v
│   ├── registerFile.v
│   ├── mux.v
│   ├── pipeline_registers.v
│   └── seven_segment.v
│
├── sim/
│   └── MIPSpipeline_tb.v
│
├── constraints/
│   └── Basys3.xdc
│
├── images/
│   ├── architecture.png
│   ├── rtl.png
│   ├── simulation.png
│   └── fpga_output.png
│
├── dissertation/
│   └── Major_Project_Report.pdf
│
└── README.md
```
# How to Run

## Vivado Implementation Steps

### Step 1: Open Vivado
Launch Xilinx Vivado Design Suite on your system.

### Step 2: Create a New Project
Create a new RTL project and select the Basys 3 FPGA board or Artix-7 device.

### Step 3: Add Verilog Source Files
Add all Verilog HDL source files including:
- MIPSpipeline.v
- ALU.v
- ControlUnit.v
- RegisterFile.v
- DataMemory.v
- ForwardingUnit.v
- SevenSegmentDisplay.v
- Testbench files

### Step 4: Add Constraints File
Add the Basys 3 FPGA constraints (.xdc) file for switch, clock, and seven-segment display pin mapping.

### Step 5: Run Synthesis
Run synthesis to generate the RTL schematic and hardware logic optimization results.

### Step 6: Run Implementation
Run implementation for placement, routing, and timing optimization on the FPGA device.

### Step 7: Generate Bitstream
Generate the FPGA programming bitstream file (.bit).

### Step 8: Program Basys 3 FPGA
Connect the Basys 3 board through USB and program the FPGA using Vivado Hardware Manager.

### Step 9: Verify Hardware Output
Use FPGA switches to select different operations and observe outputs on the seven-segment display.

# Future Improvements

The proposed pipelined MIPS processor architecture can be further enhanced by integrating advanced processor and hardware acceleration features. Some possible future improvements are listed below:

## Floating Point Unit (FPU)
Addition of IEEE-754 compliant floating-point arithmetic support for scientific and DSP applications.

## Cache Memory
Implementation of instruction and data cache memory to improve processor speed and reduce memory access latency.

## Advanced Hazard Prediction
Integration of branch prediction and advanced hazard management techniques for improved pipeline efficiency.

## AI Accelerator Integration
Incorporation of lightweight AI acceleration modules for machine learning and neural network applications.

## DSP Extensions
Addition of Digital Signal Processing instructions such as MAC operations and vector arithmetic.

## Larger Matrix Multiplication Support
Extension of the arithmetic accelerator to support higher-order matrix multiplication operations such as 3×3 and 4×4 matrices.

## UART and Peripheral Interfaces
Integration of UART, SPI, and I2C communication protocols for external hardware interfacing.

## Power Optimization
Implementation of low-power pipeline techniques and clock-gating methods for reduced FPGA power consumption.

## Multi-Core Expansion
Future extension of the processor architecture into a multi-core FPGA-based processing system.
[MIPSpipelineFinal.zip](https://github.com/user-attachments/files/28230633/MIPSpipelineFinal.zip)
# Authors

## Project Developed By

### Sandeep Kumar
- B.Tech Electronics and Communication Engineering
- Roll No.: 22134502012


Department of Electronics and Communication Engineering  
School of Engineering and Technology (SOET)  
Hemvati Nandan Bahuguna Garhwal University  
Srinagar Garhwal, Uttarakhand
