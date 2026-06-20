# Basic Computer Control Unit

A custom hardwired control unit built in Logisim, extending a Mano-architecture "basic computer" to execute a specific instruction subset — including two custom instructions added on top of the standard set.

Built for the Computer Organization & Systems Programming course (CSEN/CSIS402), German University in Cairo.

## Overview

- Implements **LDA, STA, ADD, BUN, ISZ**, plus two custom instructions: **XOR** (logical XOR between the accumulator and a memory operand) and **DIV** (integer division between the accumulator and a memory operand)
- Full RTL-level control design — every register's Load / Increment / Clear signal derived as a Boolean expression across time states T0–T6
- Hardwired control unit: decoder-based instruction decoding, a bus-select-line encoder, and an ALU-operation-select encoder, each with derived logical (SOP) expressions
- Validated end-to-end against a test assembly program containing a loop with conditional branching

## Test Program

```assembly
ORG 0
LOP, LDA A
     XOR B
     ADD A
     STA A
     LDA A
     DIV B
     ADD C
     STA C
     ISZ i
     BUN LOP
     HLT
A, DEC 15
B, DEC 5
C, DEC 0
i, DEC -3
```

Equivalent high-level logic:

```c
for (i = 0; i < 3; i++) {
    A += A XOR B;
    C += A / B;
}
```

With initial values A = 15, B = 5, C = 0, the circuit correctly produces the expected final values **A = 101, C = 35**.

## Design Highlights

- **Register control:** Load/Increment/Clear logic derived per register (DR, AR, IR, AC, PC, SC) from the instruction decoder outputs (D0–D6) and time states
- **Memory control:** Read and write enable signals derived from the same decoder/timing logic
- **Bus select encoder:** 3-bit select logic (S0–S2) routing Memory, AR, PC, DR, AC, or IR onto the common bus
- **ALU select encoder:** 3-bit select logic (C0–C2) choosing between XOR, ADD, DIV, and PASS-through operations
- Synchronous CLR handling for counter-based registers using an edge-triggered flip-flop, as required by Logisim's asynchronous counter clear behavior

## Files

- `Team36.circ` — Logisim circuit file (open directly in Logisim)
- `CO report.pdf` — Full RTL design report: timing diagrams, control signal expressions, bus/ALU encoder logic, and memory contents
- `Names&IDS.pdf` — Team member list

## Tech Stack

`Logisim` · `Digital Logic Design` · `RTL / Register Transfer Level Design` · `Control Unit Design` · `Computer Architecture`
