---
title: Sample Spaces with Equally Likely Outcomes
---

If all outcomes in a sample space $S$ are equally likely, then for an event $E$,

$$
P(E)=\frac{|E|}{|S|}
$$

So many probability problems reduce to **counting the number of favorable outcomes and total outcomes**.

---

# Example: Drawing Balls from an Urn

An urn contains:

- 7 white balls
- 5 black balls

Three balls are drawn at random.

Find the probability of drawing **1 white and 2 black**.

## Method 1: Order Does Not Matter

The total number of ways to choose 3 balls from 12 is

$$
|S|
=
\binom{12}{3}
$$

The number of favorable selections is

$$
|E|
=
\binom{7}{1}\binom{5}{2}
$$

Therefore,

$$
P(E)
=
\frac{\binom{7}{1}\binom{5}{2}}
{\binom{12}{3}}
=
\frac{7}{22}
$$

---

## Method 2: Order Matters

There are

$$
12\cdot11\cdot10
$$

possible ordered draws.

The white ball can appear in any of the 3 positions:

$$
7\cdot5\cdot4
$$

ways for each position.

Therefore,

$$
|E|
=
3\cdot7\cdot5\cdot4
$$

and

$$
P(E)
=
\frac{3\cdot7\cdot5\cdot4}
{12\cdot11\cdot10}
=
\frac{7}{22}
$$

> Whether order is included or ignored, the final probability is the same as long as the counting method is consistent.

---

# Matching Problem

Suppose $n$ people each throw their hat into a pile and randomly select one hat.

Let

$$
E_i
=
\{\text{person }i\text{ gets their own hat}\}
$$

The total number of possible hat assignments is

$$
n!
$$

We want the probability that **no one gets their own hat**.

That event is

$$
E_1^cE_2^c\cdots E_n^c
$$

Using complements,

$$
P(E_1^cE_2^c\cdots E_n^c)
=
1-P(E_1\cup E_2\cup\cdots\cup E_n)
$$

---

# Inclusion-Exclusion in the Matching Problem

Using the inclusion-exclusion principle,

$$
P(E_1\cup\cdots\cup E_n)
=
\frac{1}{1!}
-\frac{1}{2!}
+\frac{1}{3!}
-\cdots
+\frac{(-1)^{n+1}}{n!}
$$

Therefore,

$$
P(\text{no one gets their own hat})
=
1-\frac{1}{1!}
+\frac{1}{2!}
-\frac{1}{3!}
+\cdots
+\frac{(-1)^n}{n!}
$$

This is a truncated Taylor series for

$$
e^{-1}
$$

so for large $n$,

$$
P(\text{no one gets their own hat})
\approx
e^{-1}
\approx
0.369
$$

So even with many people, the probability that nobody gets their own hat approaches about

$$
36.9\%
$$
