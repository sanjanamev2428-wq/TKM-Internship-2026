# AES-128 Optimization

## Project Overview

This project focuses on optimizing an AES-128 (Advanced Encryption Standard) encryption core implemented in Verilog RTL. The original design was based on a fully unrolled AES architecture containing dedicated hardware for all encryption rounds and key expansion stages.

The objective of this work was to reduce FPGA resource utilization, power consumption, and hardware complexity while maintaining complete AES-128 functionality and timing closure.

## Reference Design

Original AES-128 implementation:

https://github.com/Shehab-Naga/AES-128

## Optimization Goals

- Reduce LUT utilization
- Reduce Flip-Flop utilization
- Lower dynamic power consumption
- Maintain AES-128 functional correctness
- Meet 100 MHz timing requirements
- Follow an industry-style resource-sharing architecture

---

# Implemented Optimizations

## 1. Iterative Round Reuse

### Original Design

The original AES core instantiated separate hardware for each encryption round.<br>
Round1 -> Round2 -> Round3 -> ... -> Round10

### Optimized Design

A single AES Round module is reused across all rounds using an FSM-controlled iterative architecture.<br>
+---------+
State --->| Round |----+
+---------+ |
^ |
| |
+---------+
### Benefits

- Significant area reduction
- Lower LUT utilization
- Reduced power consumption
- Simpler hardware architecture

---

## 2. On-the-Fly Key Expansion

### Original Design

Multiple KeyExpansion modules generated all round keys simultaneously.

### Optimized Design

A single reusable KeyExpansion module generates round keys dynamically during encryption.

Features:

- Round counter
- Rcon lookup table
- Single KeyExpansion hardware block

### Benefits

- Reduced hardware resources
- Lower register count
- Improved synchronization with encryption rounds

---

## 3. MixColumns Optimization

The MixColumns implementation was optimized by sharing intermediate computations and eliminating redundant XOR operations.

### Optimization Technique

Compute:
T = a0 ⊕ a1 ⊕ a2 ⊕ a3

once and reuse it for all output calculations.

### Benefits

- Reduced combinational logic
- Lower logic depth
- Improved timing performance

---

# Results

## Resource Utilization

| Metric | Improvement |
|----------|------------|
| LUT Usage | ~85% Reduction |
| Flip-Flops | Significant Reduction |
| Routing Complexity | Reduced |
| Area Utilization | Reduced |

---

## Latency

| Design | Clock Cycles |
|----------|------------|
| Original Unrolled Architecture | 21 Cycles |
| Optimized Iterative Architecture | 31 Cycles |

The increase in latency is an accepted trade-off for substantial area and power savings.

---

## Timing Analysis

| Parameter | Value |
|------------|--------|
| Clock Frequency | 100 MHz |
| Clock Period | 10 ns |
| WNS | +6.061 ns |
| WHS | +0.083 ns |

### Timing Status

✔ No setup violations

✔ No hold violations

✔ Timing closure achieved at 100 MHz

---

## Power Analysis

| Metric | Before | After |
|----------|--------|--------|
| Total Power | 0.650 W | 0.182 W |
| Dynamic Power | 0.536 W | 0.070 W |

### Improvements

- Total Power Reduction ≈ 72%
- Dynamic Power Reduction ≈ 87%

---

# Verification

A SystemVerilog verification environment was developed consisting of:

- Generator
- Driver
- Monitor
- Scoreboard
- DUT

### Verification Checks

- AES standard compliance
- NIST test vectors
- Boundary condition testing
- Output correctness
- Latency verification

### Results

| Metric | Result |
|----------|--------|
| Total Test Cases | 10 |
| Passed | 10 |
| Failed | 0 |
| Pass Rate | 100% |

---

## Sample Test Vector

### Plaintext
00112233445566778899AABBCCDDEEFF

### Key
000102030405060708090A0B0C0D0E0F

### Expected Ciphertext
69C4E0D86A7B0430D8CDB78070B4C55A

Result: PASS ✓

---

# Tools Used

- Verilog HDL
- SystemVerilog
- Vivado
- FPGA Synthesis & Implementation
- Timing Analysis
- Power Analysis

---

# Author

**Sanjana M**

Electronics Engineering (VLSI Design & Technology)

TKM College of Engineering Internship Project (2026)

---

# Conclusion

The AES-128 encryption core was successfully optimized using iterative round reuse, on-the-fly key expansion, and MixColumns restructuring. These improvements achieved major reductions in FPGA resource utilization and power consumption while maintaining complete AES functional correctness and meeting the target operating frequency of 100 MHz.
