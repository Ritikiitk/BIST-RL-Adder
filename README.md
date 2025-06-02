# BIST-RL-Adder
## 🔍 Introduction

The increasing demand for **low-power** and **energy-efficient computing** in advanced technologies—such as **quantum computing** and **nanotechnology**—has led to the emergence of **reversible logic circuits** as a promising solution.

In this work, we propose a **Built-In Self-Test (BIST)** architecture for **low-power reversible logic adders**, designed using **Fredkin** and **Peres gates**. The architecture features:
- A **low-transition Bit Swapping Linear Feedback Shift Register (BS-LFSR)** for pseudorandom pattern generation.
- A **Multiple Input Signature Register (MISR)** for compact output response analysis.

The **reversible adder** acts as the **Circuit Under Test (CUT)**, aiming to minimize **energy dissipation** while maintaining **high test coverage**.

The design is described in **Verilog HDL** and implemented using the **Xilinx Vivado** platform.  
🔬 **Experimental results** reveal:
- A **13.61% reduction in power consumption**.
- A **power saving of approximately 0.5 W** compared to conventional LFSR-based BIST architectures.

Additionally, **simulation with stuck-at fault models** demonstrates **high fault detection efficiency** with **minimal area and performance overhead**, confirming the approach's effectiveness for **energy-efficient, self-testable logic systems**.


![Image](https://github.com/user-attachments/assets/e24d6a6e-49ea-4387-b516-1850e4fd1ddc)

# BIST Architecture for Reversible Logic Adder using Fredkin and Peres Gates

## 1. Design of Reversible Logic Adder

A reversible full adder circuit is designed using **Fredkin** and **Peres gates**, selected for their low gate count and quantum cost efficiency. These gates ensure **no fan-out and feedback**, adhering strictly to the fundamental constraints of reversible logic circuits.

---

## 2. Integration of BIST Architecture

### A) Circuit Under Test (CUT)
The BIST (Built-In Self-Test) architecture is implemented around the reversible adder as the CUT.

### B) Test Pattern Generation
A **Low Transition Linear Feedback Shift Register (LFSR)**, also known as **BS-LFSR**, is used as the **test pattern generator**, providing pseudorandom inputs to stimulate the CUT.

### C) Output Response Compression
A **Multiple Input Signature Register (MISR)** is used to compact the output responses of the CUT into a final **signature**. This signature is compared against a reference **Golden code** to detect faults.

### D) Dual-Mode Operation
The architecture supports both **normal and test modes**, controlled through **multiplexers** and **control signals** for flexible operation.

---

## 3. Fault Modeling

The CUT is analyzed for common reversible logic fault models, including:
- **Stuck-at faults**
- **Bridging faults**

Simulation is conducted to validate the **fault coverage** of the proposed BIST structure.

---

## 4. Implementation and Performance Analysis on Xilinx Vivado

### A) RTL Design and Simulation
- The complete BIST-integrated reversible adder is implemented in **Verilog**.
- Design is synthesized and simulated using **Xilinx Vivado** to verify correct logical behavior.

### B) Timing and Power Analysis
- **Static Timing Analysis** is performed to identify **propagation delays** and **timing violations**.
- **Power Reports** include analysis of both **dynamic** and **static power consumption**.

### C) FPGA Resource Utilization
- Resource metrics such as:
  - **LUTs (Look-Up Tables)**
  - **Flip-Flops**
  - **I/Os**
  
  are analyzed to assess **area efficiency** on the target FPGA.

---

## 🛠️ Tools Used
- **Xilinx Vivado**
- **Verilog HDL**

---

## 📁 Repository Structure (Optional Example)
```plaintext
├── src/
│   ├── reversible_adder.v
│   ├── lfsr.v
│   ├── misr.v
│   └── bist_top.v
├── testbench/
│

