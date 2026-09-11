---
title: MOSFET
---

MOSFET: Metal-Oxide-Semicondcutor Field-Effect Transistor

A MOSFET is a transistor that controls current using voltage. 

## 1. MOSFET Terminals

A MOSFET is usually drawn as a 3-terminal device, but physically it has **4 terminals**:

* **Gate**
* **Source**
* **Drain**
* **Body**

For many MOSFETs, the **source and drain are physically symmetric**.
However, in circuit operation, we call one side “source” and the other side “drain” depending on the applied voltages and current direction.

## 2. NMOS and PMOS Body Connection

### NMOS

An **NMOS transistor** is usually built in a **p-type body**.

This p-type body can be:

* **p-substrate**
* **p-well**

For NMOS, the body is usually connected to the **lowest voltage**, normally **ground (GND)**.

This helps keep the body-source junction reverse-biased.

### PMOS

A **PMOS transistor** is usually built in an **n-well**.

For PMOS, the body is usually connected to the **highest voltage**, normally **VDD**.

This also helps keep the body-source junction reverse-biased.

## 3. MOSFET Operation Regions

A MOSFET has three main operation regions:

1. **Cut-off**
2. **Triode / Linear**
3. **Saturation**

## 4. Cut-off Region

In cut-off, the MOSFET is mostly off.

For NMOS:

[
V_{GS} < V_{TH}
]

The gate-to-source voltage is not large enough to strongly turn on the channel, so ideally no drain current flows.

In real devices, a very small leakage current can still flow.

## 5. Triode / Linear Region

In triode region, the MOSFET is on, but it behaves more like a **voltage-controlled resistor**.

For NMOS:

[
V_{GS} > V_{TH}
]

and

[
V_{DS} < V_{GS} - V_{TH}
]

In this region, the MOSFET has an on-resistance called:

[
R_{on}
]

This region is often used when the MOSFET acts like a switch or resistor.

## 6. Saturation Region

In saturation region, the MOSFET behaves more like a **current source**.

For NMOS:

[
V_{GS} > V_{TH}
]

and

[
V_{DS} > V_{GS} - V_{TH}
]

Ideally, once the MOSFET enters saturation, the drain current becomes almost constant even if (V_{DS}) increases.

This is very important in analog circuits because amplifiers need a stable operating current.

## 7. Why Saturation Matters in Analog Circuits

In analog design, we often want MOSFETs to operate in the **saturation region**.

The reason is that in saturation, the drain current is mainly controlled by (V_{GS}), not (V_{DS}).

So even if (V_{DS}) changes, the current stays relatively stable.
This makes it possible to define a stable **DC operating point**, and then analyze small AC signal changes around that point.

In simple terms:

> DC analysis decides where the transistor sits.
> AC analysis studies how the circuit responds to small changes around that point.

## 8. Three Important MOSFET Effects

Real MOSFETs are not ideal.
There are three important non-ideal effects:

1. **Channel Length Modulation, CLM**
2. **Body Effect**
3. **Parasitic Capacitance**

## 9. Channel Length Modulation, CLM

Ideally, in saturation, drain current should stay constant as (V_{DS}) increases.

But in real MOSFETs, the drain current slightly increases as (V_{DS}) increases.

This effect is called **channel length modulation**.

It becomes stronger when the channel length is shorter.
So from the CLM point of view, using a longer channel length can make the current source more ideal.

In equations, CLM is often modeled using (\lambda):

[
I_D = I_{D,sat}(1 + \lambda V_{DS})
]

The parameter (\lambda) represents how much the current increases with (V_{DS}).

## 10. Body Effect

The **body effect** happens when the body voltage is different from the source voltage.

For NMOS, the body is usually connected to ground.
If the source is also at ground, then:

[
V_{SB} = 0
]

So there is no body effect.

But if the source voltage is not equal to the body voltage, then:

[
V_{SB} \neq 0
]

The threshold voltage (V_{TH}) changes.

In simple terms:

> Body effect means the body-source voltage changes the threshold voltage.

## 11. Parasitic Capacitance

Parasitic capacitance is unwanted capacitance that naturally appears inside the MOSFET.

Whenever two conductive regions are separated by an insulating material, capacitance can form.

In MOSFETs, parasitic capacitances can appear between terminals such as:

* Gate–Source
* Gate–Drain
* Drain–Body
* Source–Body

These capacitances are usually unwanted because they affect speed, delay, and coupling.

Parasitic capacitance is strongly affected by the transistor **width**.
Larger width usually creates larger parasitic capacitance.

## 12. DC Analysis

DC analysis finds the **DC operating point** of the circuit.

For example, in a common-source amplifier, if (V_{in}) is below (V_{TH}), the NMOS is off and almost no current flows.

Then:

[
V_{out} \approx V_{DD}
]

As (V_{in}) increases above (V_{TH}), the NMOS turns on, current flows through the resistor, and (V_{out}) starts to decrease.

To build an amplifier, we usually choose (V_{in}), (R_D), and the MOSFET size so that the transistor operates in saturation.

A key goal in analog design is:

> Bias the transistors so they operate in the correct region, usually saturation.

## 13. AC Analysis

After the DC operating point is set, AC analysis studies how small input changes are amplified.

The MOSFET can be replaced by a small-signal model.

Important small-signal parameters include:

### Transconductance

[
g_m
]

This tells how much the drain current changes when (V_{GS}) changes.

In simple terms:

> (g_m) tells how strongly the MOSFET converts voltage change into current change.

### Output Resistance

[
r_o
]

This comes from channel length modulation.
If CLM is small, (r_o) is large, and the MOSFET behaves more like an ideal current source.

### Body Transconductance

[
g_{mb}
]

This comes from body effect.
It models how changes in (V_{BS}) affect the drain current.

## Summary

A MOSFET is a voltage-controlled current device.

In digital circuits, it is often used as a switch.
In analog circuits, it is biased at a proper DC operating point and used as a controlled current source.

The most important analog idea is:

> Set the MOSFET in saturation for DC bias, then use small-signal analysis to understand AC amplification.
