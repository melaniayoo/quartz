---
title: Analog/Digital Signals
---

Electronic systems represent information using **analog** or **digital** signals.

# Analog Signal

An analog signal changes continuously over time.

It can have any value within a range.

Examples include:

* sound from a microphone
* temperature
* light intensity
* pressure
* battery voltage

```text
Voltage
  │      /‾\      /‾\
  │     /   \____/   \
  │____/______________\___ Time
```

A real-world signal is often analog because physical quantities change continuously.

# Digital Signal

A digital signal uses separate values instead of a continuous range.

In digital electronics, information is usually represented using two states:

```text
0 and 1
```

These states are represented by voltage ranges.

For example:

```text
Low voltage  → 0
High voltage → 1
```

```text
Voltage
  │    ┌─────┐       ┌─────┐
  │    │     │       │     │
  │____┘     └_______┘     └___ Time
```

Digital signals are used by:

* computers
* [[CPU|CPUs]]
* [[MCU|MCUs]]
* memory
* communication systems

# Analog vs. Digital

| Analog                                               | Digital                              |
| ---------------------------------------------------- | ------------------------------------ |
| Changes continuously                                 | Uses discrete values                 |
| Can have many possible values                        | Usually represented by `0` and `1`   |
| Common in real-world signals                         | Common inside computers              |
| More directly affected by [[noise]]                    | Easier to store and process reliably |

# Conversion

An ADC converts an analog signal into digital data.

```text
Analog signal → ADC → Digital data
```

A [[DAC]] converts digital data into an analog signal.

```text
Digital data → DAC → Analog signal
```

# Example

In a digital audio system:

```text
Sound
  ↓
Microphone
  ↓
Analog signal
  ↓
ADC
  ↓
Digital processing
  ↓
DAC
  ↓
Analog signal
  ↓
Speaker
```
