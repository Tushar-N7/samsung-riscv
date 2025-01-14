# RISC-V Project Analysis

## Overview

This project involves analyzing the RISC-V assembly code generated from a custom application. The analysis focuses on identifying unique instructions, decoding their formats, and interpreting their functionality.

## Steps Completed

1. Generated RISC-V Assembly:  
   Using `riscv-objdump`, the application code was disassembled to extract the RISC-V assembly instructions.

2. Identified Unique Instructions:  
   Fifteen unique RISC-V instructions were identified from the disassembled output.

3. Decoded 32-bit Instruction Codes:  
   Each instruction was analyzed to determine its exact 32-bit binary representation based on its instruction type format (e.g., R-type, I-type, S-type, etc.).

4. Documented Instruction Details:  
   For each instruction:
   - Mnemonic: The assembly-level representation (e.g., `add`, `lw`, `beq`).
   - Binary Encoding: The 32-bit binary code derived from its format and operands.
   - Instruction Type: Categorization (e.g., R-type, I-type).
   - Functionality: A brief explanation of what the instruction does.

## Example Instruction Breakdown

Instruction: `add x5, x6, x7`  
- Binary Encoding: `0000000 00111 00110 000 00101 0110011`  
- Instruction Type: R-type  
- Description: Adds the values in `x6` and `x7` and stores the result in `x5`.

## Purpose:

This repository serves as a reference for understanding RISC-V instruction encoding and functionality. It showcases the process of decoding and interpreting RISC-V instructions, bridging the gap between assembly-level programming and binary encoding. 
