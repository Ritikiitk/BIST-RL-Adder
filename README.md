# BIST-RL-Adder
The increasing demand for low-power and energy-
efficient computing in advanced technologies such as quantum
computing and nanotechnology has led to the emergence of
reversible logic circuits as a promising solution.

we propose a Built-In Self-Test (BIST) architecture for low-
power reversible logic adders using Fredkin and Peres gates.
The architecture integrates a low-transition Bit Swapping Linear
Feedback Shift Register (BS-LFSR) for pseudorandom pattern
generation and a Multiple Input Signature Register (MISR) for
compact response analysis.

The reversible adder serves as the Circuit Under Test (CUT), targeting minimal energy dissipation
while ensuring high test coverage. The design is described in
Verilog and implemented on the Xilinx Vivado platform. Experi
mental results show that the proposed BIST framework achieves
a 13.61% reduction in power consumption and a power saving
of approximately 0.5 W compared to conventional LFSR-based
designs. 
Simulation with stuck-at fault models confirms high
fault detection efficiency with minimal area and performance
overhead, demonstrating the suitability of the approach for
energy-efficient, self-testable logic systems.

1. Design of Reversible Logic Adder
A reversible full adder circuit is designed using Fredkin and Peres gates, which are chosen for their
low gate count and quantum cost efficiency to ensures no fan-out and feedback, adhering to the
fundamental constraints of reversible logic circuits.
2. Integration of BIST Architecture
 The BIST architecture is implemented around the reversible adder (Circuit Under Test - CUT).
 Utilization of low transition Linear Feedback Shift Register (LFSR) also called as BS-LFSR as
the test pattern generator, generating pseudorandom patterns to stimulate the CUT.
 A Multiple Input Signature Register (MISR) is employed to compact the output responses into a
final signature, which is compared against a reference( Golden code) to detect faults.
Page 2
 The architecture is designed to operate in both normal and test modes using multiplexers and
control signals.
3. Fault Modeling
The CUT is analyzed for common fault models applicable to reversible logic, including stuck-at
faults and bridging faults. Simulation is conducted to validate the fault coverage of the proposed
BIST structure.
4. Implementation and Performance Analysis on Xilinx Vivado
 The complete BIST integrated reversible adder is described in Verilog and synthesized using
Xilinx Vivado. The RTL design is verified through simulation to ensure correct logical behavior.
 Static timing analysis identified propagation delays and timing violations. Power reports
highlighted dynamic and static power usage. Resource utilization metrics, including LUTs, flipflops,
and I/Os, assessed area efficiency on the FPGA.
