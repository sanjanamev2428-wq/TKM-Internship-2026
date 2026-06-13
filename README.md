# Summer Internship 2026 - TKM College of Engineering

## About

This repository contains the Verilog HDL designs, testbenches, and documentation developed during the Summer Internship 2026 conducted at TKM College of Engineering (TKMCE).

## Student Details

- Name: Sanjana M
- Department: Electronics and Communication Engineering
- College: Saintgits College of Engineering
- Internship Venue: TKM College of Engineering (TKMCE)

## Internship Details

- Internship Name: Summer Internship 2026
- Duration: 15 Days
- Start Date: 08 June 2026
- Tool Used: Vivado Design Suite
- Hardware Description Language: Verilog HDL

## Repository Structure

```text
TKM_INTERNSHIP
│
├── README.md
│
└── Day1
    ├── Ripple_Carry_Adder
    │   ├── Design
    │   ├── Testbench
    │   └── rca.md
    │
    └── BCD_Counter
        ├── Design
        ├── Testbench
        └── bcd.md
```

## Experiments Completed

### Day 1
- 4-Bit Ripple Carry Adder
- BCD Counter
  
# Day 2: Decoders, Flip-Flops & Shift Registers

## Overview
This repository contains the Verilog RTL design and testbenches for basic combinational and sequential logic circuits. This design assignment is structured as part of the VLSI & Chip Design Summer Internship at TKM College of Engineering.

## Projects Included
This folder contains the design and documentation for four types of circuits:

1. **4x2 Decoder**
   * A combinational logic circuit that decodes 2 binary inputs into 4 distinct outputs.
   * **Documentation:** [Decoder Readme](./4x2_Decoder/decoder.md)

2. **D Flip-Flop**
   * A sequential logic circuit that tracks the input data at the active clock edge.
   * **Documentation:** [D FF Readme](./D_Flip-Flop/d_ff.md)

3. **SR Flip-Flop**
   * A basic sequential logic circuit used to store 1-bit of data using Set and Reset inputs.
   * **Documentation:** [SR FF Readme](./SR_FlipFlop/sr_ff.md)

4. **Universal Shift Register (USR)**
   * A sequential circuit capable of shifting data both left and right, along with parallel data loading.
   * **Documentation:** [USR Readme](./Universal_Shift_Register/usr.md)

## Directory Structure
```text
DAY2/
├── 4x2_Decoder/
│   ├── decoder.md
│   ├── decoder.v
│   └── tb_decoder.v
├── D_Flip-Flop/
│   ├── d_ff.md
│   ├── d_ff.v
│   └── tb_d_ff.v
├── SR_FlipFlop/
│   ├── sr_ff.md
│   ├── sr_ff.v
│   └── tb_sr_ff.v
├── Universal_Shift_Register/
│   ├── tb_usr.v
│   ├── usr.md
│   └── usr.v
└── README.md
**How to Run in Vivado**
1.Open Xilinx Vivado and create a new RTL project.

2.Add the respective .v design files (e.g., decoder.v, d_ff.v, etc.) as Design Sources.

3.Add the corresponding testbench files (e.g., tb_decoder.v, tb_d_ff.v, etc.) as Simulation Sources.

4.Click on Run Simulation -> Run Behavioral Simulation from the Flow Navigator to view the waveforms.

### Day 3
Face Detector
Sequence Detector

### Day 4
Block Memory Generator

### Day 5
Bcd Adder Interface
FIFO Interface

## Technologies Used

- Verilog HDL
- Vivado Design Suite
- GitHub

## Purpose

This repository is maintained to document and organize all designs, simulations, testbenches, and reports completed during the internship.
