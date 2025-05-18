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
├── 32 Bit MUX                     # 32-bit 2:1 multiplexer
├── 5 Bit MUX                      # 5-bit 2:1 multiplexer
├── 9 Bit MUX                      # 9-bit 2:1 multiplexer
├── ALU                            # Arithmetic Logic Unit
├── ALU Control                    # Determines ALU operation from ALUOp and funct fields
├── CPU                            # Top-level CPU architecture integrating all components
├── CPU Instructions (MIPS)        # Human-readable MIPS instructions
├── CPU Instructions (Machine Code)# Corresponding machine code for instruction ROM
├── CPU Testbench                  # VHDL testbench for simulation and validation
├── Control                        # Main control unit generating control signals
├── RAM Generation                 # Data memory (RAM) for load/store operations
├── ROM Generation                 # Instruction memory (ROM)
├── Register File                  # 32-register file with read/write access
