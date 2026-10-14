# 4-bit Arithmetic Logic Unit (ALU) - Vivado RTL Design

A synthesizable 4-bit Arithmetic Logic Unit (ALU) implemented in Verilog HDL, verified through behavioral simulation using AMD Vivado.

---

## 📌 Features

- **4-bit Data Width:** Processes two 4-bit inputs (`Operand A` and `Operand B`) to generate a 4-bit result[cite: 8].
- **Arithmetic & Logic Operations:** Supported via 3-bit control input (`alu_ctrl`)[cite: 8]:
  - `000`: Addition (`ADD`)[cite: 8]
  - `001`: Subtraction (`SUB`)[cite: 8]
  - `010`: Bitwise AND[cite: 8]
  - `011`: Bitwise OR[cite: 8]
  - `100`: Bitwise XOR[cite: 8]
  - `101`: Bitwise NOT[cite: 8]
  - `110`: Pass Operand[cite: 8]
- **Status Flags Generation:**
  - **Zero Flag (Z):** Asserted when the 4-bit computation result is `4'b0000`[cite: 8].
  - **Carry Flag (C):** Indicates unsigned overflow in addition or no-borrow condition in subtraction (ARM convention)[cite: 8].

---

## 🛠 Project Structure

```text
├── rtl/
│   └── alu_4bit.v       # Top-level synthesizable RTL code
├── tb/
│   └── tb_alu_4bit.v    # Self-checking testbench
└── sim/
    └── waveform.wcfg    # Vivado simulation waveform configuration
