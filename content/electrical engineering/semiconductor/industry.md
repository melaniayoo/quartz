---
title: Semiconductor Industry
---

Digital systems ultimately process information using **binary values: 0 and 1**.
Electronic circuits can represent these values using switches that are either ON or OFF.
A transistor works like a very small electronic switch.

By placing billions of transistors on a small semiconductor chip, the chip can perform complex calculations, process information, and store data.

# Main Types of Semiconductor Chips

## Memory Semiconductor

Memory chips are mainly used to **store information**.

Examples:

* [[DRAM]]
* [[NAND Flash]]

Major companies:

* Samsung Electronics
* SK hynix

## System Semiconductor

System semiconductors are mainly used to **process information and perform calculations**.

Examples:

* [[CPU]]
* [[GPU]]
* AP
* [[SoC]]

Major companies include:

* Intel
* AMD
* NVIDIA

# Semiconductor Company Types

## IDM

IDM stands for **Integrated Device Manufacturer**.
(design --> production --> sales)
An IDM company designs and manufactures its own semiconductor chips.

Examples:

* Samsung Electronics
* Intel
* SK hynix

```text
Design + Manufacturing
        ↓
       IDM
```

## Fabless

A **fabless company** specializes mainly in semiconductor design.

It does not operate large-scale semiconductor manufacturing facilities.

Examples:

* AMD
* NVIDIA
* Qualcomm

```text
Chip Design
    ↓
Fabless Company
    ↓
Foundry Manufacturing
```

## Foundry

A **foundry** manufactures semiconductor chips designed by other companies.

A major example is:

* TSMC

TSMC is a Taiwanese semiconductor company and one of the world's major semiconductor foundries.

## Design House

A bridge that connects a fabless and foundry. It optimizes fabless company's design so that it's suitable for production facilities at foundry. 

## IP Companies

They provide specific designs called "Cell Library" to a fabless. IP companies only sell design licenses and does not manufacture products of its own brand. 

## OSAT

Outsourced Semiconductor Assembly and Test companies, they handle testing and packaging semiconductors from foundaries. 

### ASML

ASML is a company that produces advanced equipment used in semiconductor manufacturing.

Its photolithography machines allow extremely small circuit patterns to be transferred onto wafers.

Smaller patterns make it possible to place more transistors in a limited chip area.

# Simple Industry Structure

```text
Fabless
  │
  │ designs chips
  ↓
Foundry
  │
  │ manufactures chips
  ↓
Finished Semiconductor Chip
```

An IDM performs both design and manufacturing within the same company.
