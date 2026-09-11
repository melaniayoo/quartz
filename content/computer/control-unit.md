---
title: Control Unit
---

The Control Unit is a part of the [[CPU]] that directs how an instruction is executed.

It reads the instruction and generates **control signals** that tell other components what to do.

# Main Role

The Control Unit can control:

* the [[ALU]]
* registers
* memory
* multiplexers
* the program counter

For example, it determines whether the CPU should:

* perform an ALU operation
* read from memory
* write to memory
* store a result in a register
* branch to another instruction

# Control Signals

In a RISC-V processor, common control signals include:

* `RegWrite`
* `MemRead`
* `MemWrite`
* `MemToReg`
* `ALUSrc`
* `ALUOp`
* `Branch`

The values of these signals depend mainly on the instruction's **opcode**.

# Example

For an addition instruction:

```text
add x3, x1, x2
```

the Control Unit tells the CPU to:

1. read `x1` and `x2`
2. send both values to the ALU
3. perform addition
4. write the result into `x3`

# Simple Diagram

```text
Instruction
    ↓
┌────────────────┐
│  Control Unit  │
└────────────────┘
   ↓    ↓    ↓
 ALU  Memory  Registers
```

# Key Idea

The Control Unit does not perform the calculation itself.

It generates the signals that coordinate the datapath and make the instruction execute correctly.
