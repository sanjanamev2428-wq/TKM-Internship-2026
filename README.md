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
```
## Day3: FIFO Usecase,Sequence detector

* FIFO Usecase
  
1.Designed and verified an 8 \times 8 synchronous FIFO buffer in Verilog to manage data transfer rate-matching between a high-speed data source module and a slower processing destination module.​
Integrated status tracking flags (full and empty) alongside internal pointer controls to secure data integrity and buffer pipeline data bursts without loss over varying execution cycles.

* Sequence detector

1.Constructed a finite state machine (FSM) to continuously monitor serial data streams for a targeted bit pattern.

2.Evaluated overlapping or non-overlapping state sequence transitions to guarantee reliable pattern recognition.
## Day4: Block memory generator

* Engineered a synchronous single-port RAM architecture featuring parameterized byte-wide data paths and independent address tracking.
* Integrated an asynchronous active-low reset loop to safely initialize the internal memory matrix configurations.

## Day5:FIFO interfacing,BCD interfacing

* FIFO Interfacing
Rectified status flag generation logic using a dynamic element counter to unlock 100% buffer capacity, resolving critical boundary alignment bugs between read/write pointer wraparounds.
* BCD Interfacing
Engineered and integrated binary-coded decimal communication logic to facilitate synchronized, multi-digit numeric data conversions and stable display-driver interactions.

## Day6:FIFO transaction class

**How to Run in Vivado**

1.Open Xilinx Vivado and create a new RTL project.

2.Add the respective .v design files (e.g., decoder.v, d_ff.v, etc.) as Design Sources.

3.Add the corresponding testbench files (e.g., tb_decoder.v, tb_d_ff.v, etc.) as Simulation Sources.

4.Click on Run Simulation -> Run Behavioral Simulation from the Flow Navigator to view the waveforms.

## Technologies Used

- Verilog HDL
- Vivado Design Suite
- GitHub

## Purpose

This repository is maintained to document and organize all designs, simulations, testbenches, and reports completed during the internship.

