---
title: ADC/DAC
---

ADC and DAC connect analog signals with digital systems.

```text
Analog signal → ADC → Digital data
Digital data → DAC → Analog signal
```

# ADC

ADC stands for **Analog-to-Digital Converter**.

It converts a continuous analog signal into digital values that a processor can read.

# How It Works

An ADC:

1. samples the analog signal
2. measures its voltage
3. converts the measurement into a binary number

```text
Sensor voltage
      ↓
     ADC
      ↓
Binary data
      ↓
Processor
```

# Main Uses

ADCs are used with:

* microphones
* temperature sensors
* pressure sensors
* cameras

# Resolution

Resolution determines how many digital levels the ADC can represent.

An `n`-bit ADC has:

$$
2^n
$$

possible output levels.

For example:

```text
8-bit ADC  → 256 levels
10-bit ADC → 1024 levels
12-bit ADC → 4096 levels
```

Higher resolution allows smaller voltage differences to be measured.

# DAC

DAC stands for **Digital-to-Analog Converter**.

It converts digital data into an analog voltage or current.

# How It Works

A DAC receives a binary value and produces a corresponding analog output.

```text
Digital data
      ↓
     DAC
      ↓
Analog voltage
      ↓
Speaker or circuit
```

# Main Uses

DACs are used in:

* audio systems
* headphones
* speakers
* video equipment
* motor control
* signal generators

# ADC vs. DAC

| ADC                       | DAC                                 |
| ------------------------- | ----------------------------------- |
| Analog to digital         | Digital to analog                   |
| Used for inputs           | Used for outputs                    |
| Reads sensors and signals | Drives speakers and analog circuits |
| Produces binary data      | Produces voltage or current         |
