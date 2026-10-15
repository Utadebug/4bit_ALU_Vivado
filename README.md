# 4-bit Arithmetic Logic Unit (ALU) - Vivado RTL Design

A synthesizable 4-bit Arithmetic Logic Unit (ALU) implemented in Verilog HDL, verified through behavioral simulation using AMD Vivado.

<img width="510" height="312" alt="Screenshot 2026-10-15 100551" src="https://github.com/user-attachments/assets/986adfab-54d3-47d4-8e21-ac17bf79cab0" />

 ## Features
- **Hybrid 10-Operation ALU:** 
  - **Single-Cycle:** Addition, Subtraction, bitwise logic (`AND`, `OR`, `XOR`, `NOT`), and 1-bit shifts (`SHL`, `SHR`).
  - **4-Cycle Multi-Cycle:** Shift-and-Add Multiplication (`MUL`) and Restoring Division (`DIV`) with handshaking (`start`, `busy`, `done`).
- **Flag Generation:** Real-time updates for Carry (`C`), Zero (`Z`), Negative (`N`), Overflow (`V`), and Divide-by-Zero (`div_by_zero`).
- **Modular RTL:** Partitioned into dedicated functional units (`adder_sub_4bit`, `logic_unit`, `shifter_unit`, `muldiv_core`, `flag_gen`, `result_mux`).

## Verification
- **Automated Testbench (`alu_4bit_tb.v`):** 100% PASS rate across all test vectors (3,584 combinational checks + 512 sequential checks)[cite: 29].
- **Platform:** AMD Xilinx Vivado (XSim)[cite: 28, 35].

## FPGA Resource Utilization (Artix-7 xc7a35tcpg236-1)
- **LUTs:** 60 / 20,800 (0.29%)[cite: 35]
- **Flip-Flops:** 18 / 41,600 (0.04%)[cite: 35]
- **IO Pins:** 30 / 106 (28.30%)[cite: 35]
