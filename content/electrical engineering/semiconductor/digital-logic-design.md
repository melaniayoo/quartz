---
title: Digital Logic Design
---

Digital logic design is the process of creating circuits that operate using binary values:

```text
0 and 1
```

These circuits are built from components such as:

* logic gates
* multiplexers
* registers
* counters
* state machines

# RTL

RTL stands for **Register-Transfer Level**.

It describes how data moves between registers and what operations happen on each clock cycle.

For example:

```text
Register A
    ↓
   ALU
    ↓
Register B
```

RTL is commonly written using hardware description languages such as:

* Verilog
* SystemVerilog
* VHDL

# Design Flow

```text
Requirement Specification
     ↓
RTL Design
     ↓
Simulation and Verification
     ↓
Synthesis
     ↓
Physical chip implementation
```

# Key Idea

Digital logic design creates hardware that works with binary signals.

RTL is a way to describe how data is stored, transferred, and processed inside that hardware.
