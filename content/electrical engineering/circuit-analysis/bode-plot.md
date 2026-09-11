---
title: Bode Plot
---

A **Bode plot** shows how a circuit or system responds to different frequencies.

It consists of two graphs:

* **Magnitude plot** → shows gain versus frequency
* **Phase plot** → shows phase shift versus frequency

The frequency axis is usually logarithmic.

# Magnitude Plot

The magnitude plot shows how much the circuit amplifies or attenuates a signal.

Gain is commonly expressed in decibels:

$$
Gain_{dB} = 20\log_{10}|A|
$$

```text
Gain (dB)
   │─────────
   │         \
   │          \
   │           \
   └──────────────── Frequency
```

# Phase Plot

The phase plot shows how much the output signal is shifted in phase compared with the input.

```text
Phase
  0° ─────────
              \
               \
-90°            ─────
   └──────────────── Frequency
```

# What Bode Plots Are Used For

Bode plots help determine:

* gain
* bandwidth
* cutoff frequency
* frequency response
* [[Phase Margin]]
* stability

# Example: Amplifier

At low frequencies, an amplifier may have nearly constant gain.

As frequency increases, the gain eventually begins to decrease.

The **−3 dB frequency** is often used to define the amplifier's bandwidth.

# Feedback Systems

For a [[Feedback System]], Bode plots are especially useful for analyzing stability.

The magnitude and phase of the **loop gain** are used to determine quantities such as:

* gain margin
* [[Phase Margin]]
* risk of oscillation

# Key Idea

**A Bode plot shows how gain and phase change with frequency.**

```text
Bode Plot
├── Magnitude → How much?
└── Phase     → How much phase shift?
```
