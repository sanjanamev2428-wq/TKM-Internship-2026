# FIFO Interface

## Output Waveform

<img width="1600" height="238" alt="WhatsApp Image 2026-06-13 at 10 42 16 PM" src="https://github.com/user-attachments/assets/9674a46e-19e6-462e-9387-59fdcbcdbd4c" />


Synchronous FIFO Design and Verification <br>

Hi everyone I am working on a project for a 8-bit Synchronous FIFO memory buffer using Verilog, I also made a testbench in SystemVerilog style to check how it handles writing and reading data.<br> To keep the testbench clean and organized I used a SystemVerilog interface to bundle all the wires like clock, reset, data and flags between the testbench and the FIFO.

📌 Project Features<br>

Data Size: The FIFO has 8-bit inputs and outputs.<br>

Storage: It can hold, up to 8 data values.<br>

Clean Code: The FIFO uses a fifo_if interface to connect everything.<br>

Flags: It has empty indicators so it does not overflow or glitch out. The FIFO has empty flags.<br>

## Result

The FIFO Interface was successfully implemented and simulated.
