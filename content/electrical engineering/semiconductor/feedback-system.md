---
title: Feedback System
---

A **feedback system** uses part of its output and sends it back to the input.

The feedback changes how the system behaves.

```text id="fbflow1"
Input
  ↓
System
  ↓
Output
  ↓
Feedback
  └────→ back to input
```

# Negative Feedback

**Negative feedback** subtracts part of the output from the input.

It is commonly used to:

* stabilize gain
* reduce distortion
* reduce sensitivity to component variation
* improve accuracy
* increase bandwidth

Negative feedback is widely used in [op-amp] circuits.

# Positive Feedback

**Positive feedback** adds part of the output back to the input.
It can make the output change more strongly.

It is commonly used in:

* oscillators
* comparators with hysteresis
* switching circuits

Too much positive feedback can make a system unstable or cause oscillation.

# Example

In an op-amp amplifier:

```text id="fbopamp1"
Input
  ↓
Op-Amp
  ↓
Output
  ↓
Feedback Network
  └────→ Input
```

The feedback network helps determine the closed-loop gain.

# Key Idea

**Feedback = using the output of a system to influence its input.**

* Negative feedback → usually improves stability and accuracy
* Positive feedback → reinforces changes and can create switching or oscillation
