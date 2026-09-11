---
title: Axioms of Probability
---

A probability is assigned to each event $E$ and written as
$$
P[E]
$$

---

## Axiom 1: Probability Bounds

For any event $E$,

$$
0\le P(E)\le1
$$

---

## Axiom 2: Total Probability

The probability of the entire sample space is

$$
P(S)=1
$$

---

## Axiom 3: Additivity for Disjoint Events

If $E_1,E_2,\dots$ are disjoint, then

$$
P\left(\bigcup_{i=1}^{\infty}E_i\right)
=
\sum_{i=1}^{\infty}P(E_i)
$$

This means probabilities can be added directly when the events do not overlap.

---

# Consequences of the Axioms

## Empty Set

The probability of an impossible event is

$$
P(\emptyset)=0
$$

---

## Finite Additivity

If $E_1,E_2,\dots,E_n$ are disjoint,

$$
P\left(\bigcup_{i=1}^{n}E_i\right)
=
\sum_{i=1}^{n}P(E_i)
$$

---

# Equally Likely Outcomes

Suppose

$$
S=\{1,2,\dots,N\}
$$

and all outcomes are equally likely.

Then each outcome has probability

$$
P(i)=\frac{1}{N}
$$

Therefore, for any event $E\subset S$,

$$
P(E)=\frac{|E|}{|S|}
$$

where $|E|$ is the number of outcomes in $E$.

---

# Complement Rule

Since $E$ and $E^c$ are disjoint and

$$
E\cup E^c=S
$$

we get

$$
P(E)+P(E^c)=1
$$

Therefore,

$$
P(E^c)=1-P(E)
$$

This is useful for probabilities involving:
- not
- neither
- none
- at least one

---

# Monotonicity

If

$$
E\subset F
$$

then

$$
P(E)\le P(F)
$$

because $F$ contains all outcomes in $E$, possibly plus additional outcomes.

---

# Union of Two Events

For any two events $E$ and $F$,

$$
P(E\cup F)
=
P(E)+P(F)-P(E\cap F)
$$

The intersection is subtracted because it is counted twice in

$$
P(E)+P(F)
$$

## If the Events Are Disjoint

If

$$
E\cap F=\emptyset
$$

then

$$
P(E\cup F)=P(E)+P(F)
$$

---

# Example: Brakes and Tires

Let

$$
B=\{\text{needs new brakes}\}
$$

and

$$
T=\{\text{needs new tires}\}
$$

Given

$$
P(B)=0.5
$$

$$
P(T)=0.4
$$

$$
P(B\cap T)=0.3
$$

Find the probability that the car needs neither.

Using De Morgan's Law,

$$
B^c\cap T^c=(B\cup T)^c
$$

so

$$
P(B^c\cap T^c)
=
1-P(B\cup T)
$$

First,

$$
P(B\cup T)
=
0.5+0.4-0.3
=
0.6
$$

Therefore,

$$
P(\text{neither})
=
1-0.6
=
0.4
$$

---

# Union of Three Events

For three events,

$$
P(E\cup F\cup G)
=
P(E)+P(F)+P(G)
-P(EF)-P(EG)-P(FG)
+P(EFG)
$$

The pattern is:

1. Add individual probabilities.
2. Subtract pairwise intersections.
3. Add the triple intersection back.

Why?

A point in all three events is counted:

$$
3-3+1=1
$$

which is exactly once.

---

## Inclusion-Exclusion Principle

The **inclusion-exclusion principle** finds the probability that at least one of several events occurs without double-counting overlaps.

For multiple events, the pattern is:

$$
\text{add singles} - \text{subtract pairs} + \text{add triples} - \cdots
$$

---

# Quick Exam Review

## Core Axioms

$$
0\le P(E)\le1
$$

$$
P(S)=1
$$

For disjoint events,

$$
P\left(\bigcup_iE_i\right)=\sum_iP(E_i)
$$

---

## Important Derived Results

$$
P(\emptyset)=0
$$

$$
P(E^c)=1-P(E)
$$

$$
E\subset F
\Rightarrow
P(E)\le P(F)
$$

For equally likely outcomes,

$$
P(E)=\frac{|E|}{|S|}
$$

For two events,

$$
P(E\cup F)
=
P(E)+P(F)-P(EF)
$$

For three events,

$$
P(E\cup F\cup G)
=
P(E)+P(F)+P(G)
-P(EF)-P(EG)-P(FG)
+P(EFG)
$$

---

# Common Exam Traps

- Do not use
  $$
  P(E\cup F)=P(E)+P(F)
  $$
  unless the events are disjoint.

- Do not forget to subtract the overlap:
  $$
  P(E\cap F)
  $$

- For equally likely outcomes, use
  $$
  P(E)=\frac{|E|}{|S|}
  $$
  only when the outcomes really are equally likely.

- "Neither $E$ nor $F$" means
  $$
  (E\cup F)^c
  $$

- For three events, remember to add the triple intersection back:
  $$
  +P(EFG)
  $$

---

# Key Idea

Most of this section comes down to avoiding double counting.

For unions:

$$
\text{add probabilities}
-
\text{subtract overlap}
$$

and for more than two events, continue using the inclusion-exclusion pattern.