---
title: Phase Margin
---

**Phase margin** is a measure of how stable a negative-feedback system is.
It tells us how close the system is to oscillation.

# How It Is Measured

Phase margin is measured at the frequency where the **loop gain** becomes:

$$
|A\beta| = 1
$$

or:

$$
0\text{ dB}
$$

At that frequency:

$$
\text{Phase Margin} = 180^\circ + \text{Loop Phase}
$$

For example, if the loop phase is:

$$
-120^\circ
$$

then:

$$
PM = 60^\circ
$$

# Interpretation

* **Small phase margin**

  * less stable
  * more overshoot and ringing
  * higher risk of oscillation

* **Moderate phase margin**

  * good balance between stability and speed
  * around 45–60° is common

* **Large phase margin**

  * more stable
  * less overshoot and ringing
  * may have lower bandwidth and slower response

# Bandwidth Trade-Off

There is often a trade-off between [[Bandwidth]] and phase margin.

```text
Higher Bandwidth
→ Faster response
→ Usually lower phase margin
→ More stability risk

Higher Phase Margin
→ More stable
→ Usually lower bandwidth
→ Slower response
```

# Bode Plot

Phase margin is found using a [[Bode Plot]].

```text
Find where loop gain = 0 dB
          ↓
Check the phase
          ↓
Measure distance from -180°
          ↓
Phase Margin
```

# Key Idea

**Phase margin shows how much additional phase shift a feedback system can tolerate before becoming unstable.**

The goal is usually not to maximize phase margin, but to find a good balance between **stability, bandwidth, and response speed**.
