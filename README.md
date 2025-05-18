# Single Cycle CPU Lite

**Course:** EECE 5140 – Computer Architecture with VHDL  
**Institution:** Loyola Marymount University  
**Semester:** Spring 2025  
**Author:** Jude Rhoa  
**Instructor:** Professor Mirzaei

---

## Project Overview

This project implements a basic single cycle CPU in VHDL capable of executing a subset of MIPS instructions. The design supports arithmetic and logical operations, memory access (load/store), conditional branching, and jump instructions. Simulation is used to verify functionality using machine-coded MIPS instructions.

---

## Instruction Support

Supported instruction formats:

- R-Type Instructions: e.g., `ADD`, `SUB`, `AND`, `OR`
- I-Type Instructions: e.g., `LW`, `SW`, `BEQ`
- J-Type Instructions: e.g., `J`

Instructions are encoded in 32-bit machine code and stored in a ROM-based instruction memory module.

---

## File Structure

```plaintext
.
├── alu.vhdl                  # Arithmetic Logic Unit (supports AND, OR, ADD, SUB, SLT, etc.)
├── alu_control.vhdl          # Determines ALU operation from ALUOp and funct fields
├── mux_2to1_32bit.vhdl       # 32-bit 2:1 multiplexer
├── mux_2to1_5bit.vhdl        # 5-bit 2:1 multiplexer (for register selection)
├── mux_2to1_9bit.vhdl        # 9-bit 2:1 multiplexer (for branch/jump address selection)
├── control.vhdl              # Main control unit generating control signals based on opcode
├── register_file.vhdl        # 32-register file supporting simultaneous read and write
├── rom_generation.vhdl       # Instruction ROM with machine code initialization
├── ram_generation.vhdl       # Data memory (RAM) for LW and SW instructions
├── cpu.vhdl                  # Top-level CPU architecture integrating all modules
├── cpu_tb.vhdl               # VHDL testbench that simulates program execution
├── cpu_instructions.txt      # Machine-coded MIPS instructions loaded into ROM
