# Basic Computer Control Unit Design

## Overview
This project was developed as part of the Computer Organization & Systems Programming course at the German University in Cairo (GUC).

The objective was to extend a basic computer architecture by designing and implementing a complete control unit in Logisim. The control unit was built from RTL-level specifications and timing diagrams, generating all required control signals for instruction execution.

## Features

### Implemented Instructions
- LDA (Load Accumulator)
- STA (Store Accumulator)
- ADD (Add to Accumulator)
- BUN (Branch Unconditionally)
- ISZ (Increment and Skip if Zero)
- XOR (Custom Instruction)
- DIV (Custom Instruction)

### Control Unit Components
- Sequence Counter (SC)
- Timing Decoder
- Instruction Decoder
- Control Logic Network
- Bus Select Logic
- ALU Control Signals
- Memory Read/Write Control

## Design Process

1. Analyzed the instruction cycle and RTL micro-operations.
2. Derived control equations for each register operation.
3. Designed timing and decoding circuitry.
4. Implemented the complete control unit in Logisim.
5. Integrated the control unit with the basic computer architecture.
6. Verified functionality through assembly-language test programs.

## Testing & Verification

The design was validated using assembly programs to verify:
- Correct instruction execution
- Proper sequencing of micro-operations
- Memory access operations
- Arithmetic and logical operations
- Branching functionality
- Custom instruction behavior

## Tools Used
- Logisim
- RTL Design Methodology
- Assembly-Level Testing

## Author

Eman Eltahlawy  
Mechatronics Engineering Student  
German University in Cairo (GUC)
