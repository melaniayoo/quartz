---
title: DSP
---

# DSP

DSP stands for Digital Signal Processor.
It is a processor designed to quickly perform mathematical operations on digital signals.

# Signals

Real-world signals may include:

* sound
* voice
* images
* video
* temperature
* pressure
* position

These signals are usually analog.

An [[ADC]] converts the analog signal into digital data before it is processed by the DSP.

# How It Works

```text
Analog signal
     ↓
ADC
     ↓
DSP
     ↓
DAC
     ↓
Analog output
```

The DSP processes the digital data using operations such as:

* addition
* subtraction
* multiplication
* filtering
* compression
* encoding and decoding

A [[DAC]] can then convert the processed digital signal back into an analog signal.

# Example

In an audio player:

1. A microphone captures an analog sound signal.
2. An ADC converts it into digital data.
3. The DSP processes or compresses the audio.
4. The data is saved in memory.
5. During playback, the DSP decodes the audio.
6. A DAC converts it back into an analog signal for the speaker.

# Main Components

A DSP usually includes:

* **Program Memory**
  * Stores the program used to process signals.
* **Data Memory**
  * Stores the signal data being processed.
* **Compute Engine**
  * Performs mathematical operations.
* **Input and Output**
  * Connects the DSP to memory, sensors, converters, and other devices.
