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

## Control Signals Generated

The control unit generates signals for:

- Register Load
- Register Increment
- Register Clear
- Memory Read
- Memory Write
- ALU Operations
- Bus Selection
- Program Counter Control

## Testing & Verification

The design was validated using multiple assembly programs to verify:

- Correct instruction execution
- Proper sequencing of micro-operations
- Memory access operations
- Arithmetic and logical operations
- Branching functionality
- Custom instruction behavior

All outputs were compared against expected results to ensure correctness.

## Tools Used

- Logisim
- RTL Design Methodology
- Assembly-Level Testing

## Repository Contents

```text
├── Logisim Design Files
├── Project Documentation
├── Test Programs
├── Screenshots
└── README.md
```

## Author

**Eman Eltahlawy**  
Mechatronics Engineering Student  
German University in Cairo (GUC)

LinkedIn: www.linkedin.com/in/eman-eltahlawy-39587137a
