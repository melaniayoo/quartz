---
title: Operational Amplifier
---

An operational amplifier, or **op-amp**, is an electronic circuit that amplifies the voltage difference between two inputs.

It has:

* a non-inverting input `+`
* an inverting input `−`
* one output

```text
Non-inverting input (+) ─┐
                         ├── Op-Amp ── Output
Inverting input (−) ─────┘
```

The basic relationship is:

$$
V_{out}=A(V_+-V_-)
$$

where `A` is the open-loop voltage gain.
The open-loop gain is usually extremely large.

# Main Uses

Op-amps can perform:

* amplification
* addition
* subtraction
* integration
* differentiation
* filtering
* signal comparison

# Ideal Op-Amp Rules

For an ideal op-amp operating with negative feedback:

1. No current flows into the inputs.

$$
I_+=I_-=0
$$

2. The two input voltages are approximately equal.

$$
V_+\approx V_-
$$

The output is limited by the positive and negative supply voltages. If the calculated output exceeds these limits, the op-amp saturates.


# Common Op-Amp Configurations

## Inverting Amplifier

The input signal is connected to the inverting terminal.

The output has the opposite polarity from the input.

$$
V_{out}=-\frac{R_f}{R_{in}}V_{in}
$$

```text
Input → Inverting amplifier → Inverted output
```

## Non-Inverting Amplifier

The input signal is connected to the non-inverting terminal.

The output has the same polarity as the input.

$$
V_{out}=\left(1+\frac{R_f}{R_g}\right)V_{in}
$$

## Voltage Follower

A voltage follower connects the output directly to the inverting input.

$$
V_{out}=V_{in}
$$

It does not increase voltage, but it isolates two circuit stages and provides current drive.

## Summing Amplifier

A summing amplifier combines multiple input voltages into one output.

For equal input resistors:

$$
V_{out}=-\frac{R_f}{R}\left(V_1+V_2+\cdots+V_n\right)
$$

It can be used for audio mixing and analog calculations.

## Differential Amplifier

A differential amplifier amplifies the difference between two input voltages.

$$
V_{out}=A(V_2-V_1)
$$

It is useful for measuring a small signal while rejecting voltage common to both inputs.

## Integrator

An integrator produces an output related to the accumulated input signal over time.

$$
V_{out}=-\frac{1}{RC}\int V_{in},dt
$$

It uses a capacitor in the feedback path.

## Differentiator

A differentiator produces an output related to how quickly the input changes.

$$
V_{out}=-RC\frac{dV_{in}}{dt}
$$

It responds strongly to rapid changes in the input signal.

## Comparator

A [[comparator]] compares two voltages without normal negative feedback.

* If `V+ > V−`, the output moves toward the positive supply.
* If `V+ < V−`, the output moves toward the negative supply.

It is commonly used for threshold detection.
