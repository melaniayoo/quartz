---
title: Semiconductor
---

A semiconductor is a material whose electrical conductivity can be controlled.
It behaves between a conductor(materials that allow current to flow) and an insulator(materials that don't allow current to flow).

# Bandgap

The bandgap is the energy required for an electron to move from the valence band to the conduction band.

$$
E_g=E_C-E_V
$$

where:

* `EC` is the conduction-band edge
* `EV` is the valence-band edge

An electron can conduct electricity after gaining enough energy to cross the bandgap.

# Material Classification

| Material      | Bandgap            | Electrical Behavior            |
| ------------- | ------------------ | ------------------------------ |
| Conductor     | Very small or none | Electrons move easily          |
| Semiconductor | Small              | Conductivity can be controlled |
| Insulator     | Large              | Very little current flows      |

Examples:

* conductors: gold, copper, iron, aluminum
* semiconductors: silicon, germanium, gallium arsenide
* insulators: glass, rubber, plastic, wood, diamond

By artificailly adding impurities into a semiconductor, you can control the flow of current. 

# Conductivity

Semiconductor conductivity depends on the number and mobility of electrons and holes.

$$
\sigma=q(n\mu_n+p\mu_p)
$$

where:

* `n` is the electron concentration
* `p` is the hole concentration
* `μn` is electron mobility
* `μp` is hole mobility

Conductivity can be controlled using [[Doping]].

# PN Junction

A PN junction is formed when P-type and N-type semiconductor regions are joined.

```text
P-type | Depletion region | N-type
holes  | few mobile       | electrons
       | carriers         |
```

Electrons and holes recombine near the junction, creating a depletion region and an internal electric field.

PN junctions are used in:

* diodes
* transistors
* LEDs
* solar cells
* photodiodes
* integrated circuits

# Common Semiconductor Materials

## Silicon

Silicon is the most widely used semiconductor.
Silicon crystal has low electrical conductivity and high resistance, so by adding impurities into it, we can make it have or not have current flow. 

It is used in:

* CPUs
* memory
* sensors
* power devices
* integrated circuits

Its bandgap is approximately:

$$
E_g\approx1.12\text{ eV}
$$

## Germanium

Germanium has high carrier mobility but also higher leakage current than silicon.

It is used in:

* SiGe transistors
* high-speed circuits
* infrared detectors

Its bandgap is approximately:

$$
E_g\approx0.66\text{ eV}
$$

## Gallium Arsenide

Gallium arsenide, or GaAs, has high electron mobility and good high-frequency performance.

It is used in:

* RF amplifiers
* radar
* satellite communication
* LEDs
* laser diodes

## Silicon Carbide

Silicon carbide, or SiC, is a wide-bandgap semiconductor used in high-voltage and high-power systems.

Common applications include:

* electric vehicles
* fast chargers
* solar inverters
* motor drives

## Gallium Nitride

Gallium nitride, or GaN, is a wide-bandgap semiconductor with high switching speed.

It is used in:

* compact chargers
* RF power amplifiers
* wireless base stations
* power converters

# Key Idea

A semiconductor has a controllable conductivity.

Its behavior can be changed using energy, temperature, electric fields, and doping.
