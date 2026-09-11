---
title: Voltage Regulator
---

A voltage regulator is a circuit that keeps its output voltage stable even when the input voltage or load current changes.

For example:

```text
Battery: 3.2–4.2 V
        ↓
Voltage regulator
        ↓
Stable 1.0 V for CPU
```

Without a regulator, too much voltage can damage a chip, while too little voltage can cause errors or shutdowns.

# Why Voltage Changes

A regulator compensates when:

* the battery voltage falls
* the processor suddenly uses more current
* the input power fluctuates
* parts of the device turn on or off

# Main Types

## Linear Regulator

A linear regulator lowers voltage by releasing excess energy as heat.

```text
3.3 V input → linear regulator → 1.8 V output
```

### Advantages

* simple
* low electrical noise
* inexpensive

### Disadvantages

* less efficient when the voltage difference is large
* produces heat

## Switching Regulator

A [[Switching Converter]] uses rapidly switching transistors, inductors, and capacitors to convert voltage efficiently.

Common types include:

* buck converter
* boost converter
* buck-boost converter

Switching regulators are usually more efficient than linear regulators, but they are more complex and produce more electrical noise.