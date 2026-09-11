---
title: Sample Spaces and Events
---

## Sample Space

The **sample space**, denoted by $S$, is the set of **all possible outcomes** of a random experiment.

### Examples

Two coin tosses:

$$
S=\{hh,ht,th,tt\}
$$

Two 6-sided dice:

$$
S=\{(i,j)\in \mathbb{Z}^2 \mid i,j\in\{1,\dots,6\}\}
$$

Two people arriving with delays between 0 and 1 hour:

$$
S=\{(x,y)\in\mathbb{R}^2\mid 0\le x\le1,\ 0\le y\le1\}
$$

---

# Events

An **event** is a subset of the sample space.

$$
E\subset S
$$

### Example

For two coin tosses,

$$
E=\{hh,tt\}
$$

represents the event that both coins have the same result.

---

# Event Operations

## Union

$$
E\cup F
$$

means **$E$ or $F$ occurs**.

$$
E\cup F=\{x\in S\mid x\in E \text{ or } x\in F\}
$$

---

## Intersection

$$
E\cap F
$$

or 
$$
EF
$$

means **both $E$ and $F$ occur**.

$$
E\cap F=\{x\in S\mid x\in E \text{ and } x\in F\}
$$

---

## Complement

$$
E^c
$$

means **$E$ does not occur**.

$$
E^c=\{x\in S\mid x\notin E\}
$$

---

## Disjoint Events

Two events are **disjoint** if they cannot occur together.

$$
E\cap F=\emptyset
$$

---

# Partition

Events $E_1,E_2,\dots,E_n$ **partition** an event $F$ if:

1. The events are mutually disjoint.
2. Their union equals $F$.

$$
F=\bigcup_{i=1}^{n}E_i
$$

So a partition breaks an event into **non-overlapping pieces that cover the entire event**.

---

# De Morgan's Laws

De Morgan's Laws describe how complements interact with unions and intersections.

## First Law

$$
\left(\bigcup_{i=1}^{n}E_i\right)^c
=
\bigcap_{i=1}^{n}E_i^c
$$

For two events:

$$
(E\cup F)^c=E^c\cap F^c
$$

Meaning:

> "Neither $E$ nor $F$ occurs."

---

## Second Law

$$
\left(\bigcap_{i=1}^{n}E_i\right)^c
=
\bigcup_{i=1}^{n}E_i^c
$$

For two events:

$$
(E\cap F)^c=E^c\cup F^c
$$

Meaning:

> "It is not true that both $E$ and $F$ occur."

---

## Important Interpretation

$$
(E\cup F)^c
$$

means **neither event occurs**.

Meanwhile,

$$
(EF)^c
$$

means **the two events do not both occur**.

These are different events.

---

# Cartesian Product

For two sets $A$ and $B$, the **Cartesian product** is

$$
A\times B
=
\{(x,y)\mid x\in A,\ y\in B\}
$$

### Example

$$
\{0,1\}\times\{0,1,2\}
$$

$$
=
\{(0,0),(0,1),(0,2),(1,0),(1,1),(1,2)\}
$$

In general,

$$
A\times B\neq B\times A
$$

because the order of the coordinates matters.

---

## Useful Shorthand

$$
A^2=A\times A
$$

For example,

$$
\mathbb{R}^2
=
\mathbb{R}\times\mathbb{R}
$$

is the set of all ordered pairs of real numbers.

Also,

$$
\{0,1\}^{10}
$$

represents all binary strings of length 10.

---

# Quick Exam Review

### Definitions

- **Sample space $S$:** all possible outcomes
- **Event $E$:** subset of the sample space
- **Union $E\cup F$:** $E$ or $F$
- **Intersection $EF$:** $E$ and $F$
- **Complement $E^c$:** not $E$
- **Disjoint:** events cannot occur together
- **Partition:** disjoint events whose union gives the full event

### Key Identities

$$
(E\cup F)^c=E^cF^c
$$

$$
(EF)^c=E^c\cup F^c
$$

$$
(E\cup F)G=EG\cup FG
$$

$$
EF\cup G=(E\cup G)(F\cup G)
$$

### Translation to Words

- $\cup$ → **or**
- $\cap$ → **and**
- $E^c$ → **not $E$**
- $\emptyset$ → **impossible event**
- disjoint → **cannot happen together**

> **Exam tip:** A large part of early probability problems is translating English statements into the correct set notation.