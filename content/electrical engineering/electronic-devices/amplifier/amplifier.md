---
title: Amplifier
---

An amplifier is an electronic circuit that makes a signal stronger.
It takes a small input signal and produces a larger output signal containing the same basic information.

```text
Small input signal
        ↓
    Amplifier
        ↓
Larger output signal
```

For example:

```text
Input:  0.01 V audio signal
Output: 1.0 V audio signal
```

# What Stronger Means

An amplifier may increase:

* voltage
* current
* power

An amplifier does not create energy from nothing.

It uses energy from a power supply and controls that energy according to the input signal.

```text
Input signal ──→ controls amplifier
Power supply ──→ provides energy
Output signal ─→ stronger signal
```

# Gain

The amount of amplification is called **gain**.

Voltage gain is:

$$
A_v=\frac{V_{\text{out}}}{V_{\text{in}}}
$$

For example:

```text
Vin  = 0.1 V
Vout = 2.0 V

Voltage gain = 2.0 / 0.1 = 20
```

The amplifier therefore has a voltage gain of `20`.

# Common Types

## Operational Amplifier

An [[Operational Amplifier]] is mainly used to amplify and process voltage signals.

Depending on the surrounding circuit, it can add, subtract, compare, integrate, or filter signals.

## Audio Amplifier

An [[Audio Amplifier]] amplifies audio-frequency signals.

It can make a weak signal powerful enough to drive headphones or a speaker.

```text
Audio source
     ↓
Audio amplifier
     ↓
Speaker
```

## RF Amplifier

An RF amplifier amplifies high-frequency signals used in wireless communication.

Common RF amplifiers include:

* **[[Power Amplifier]]**
  * Strengthens a transmitted RF signal before it reaches the antenna.
* **Low-Noise Amplifier**
  * Strengthens a weak received RF signal while adding as little noise as possible.

## Sensor Amplifier

A sensor amplifier strengthens a small sensor signal so that an [[ADC]] or processor can measure it accurately.