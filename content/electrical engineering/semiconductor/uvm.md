---
title: UVM
---

UVM stands for **Universal Verification Methodology**.
It is a standardized method for verifying digital hardware using SystemVerilog.

# Main Purpose

UVM helps engineers build reusable and organized test environments for complex hardware designs.

# Common Components

* **Sequence**
  * Generates test operations.
* **Driver**
  * Sends inputs to the hardware design.
* **Monitor**
  * Observes signals and outputs.
* **Scoreboard**
  * Compares actual results with expected results.

# Simple Flow

```text id="k2n9qp"
Sequence
   ↓
Driver
   ↓
Design Under Test
   ↓
Monitor
   ↓
Scoreboard
```

# Key Idea

UVM provides a standard structure for testing and verifying digital hardware before it is manufactured.
