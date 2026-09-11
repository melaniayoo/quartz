---
title: Basic Principle of Counting
---

# Counting

Suppose two experiments are performed.

- Experiment 1 has $$m$$ possible outcomes.
- For each outcome of Experiment 1, Experiment 2 has $$n$$ possible outcomes.

Then the total number of possible outcomes is

$$
\boxed{mn}
$$

More generally, if a process consists of several stages, multiply the number of choices available at each stage.

## Example

How many different 7-place license plates are possible if:

- the first 3 positions are letters,
- the last 4 positions are numbers,
- repetition is not allowed?

There are:

$$
26
$$
choices for the first letter,

$$
25
$$

for the second,

$$
24
$$

for the third,

and

$$
10,9,8,7
$$

choices for the four digits.

Therefore,

$$
26\cdot25\cdot24\cdot10\cdot9\cdot8\cdot7
=
\boxed{78,\!624,\!000}
$$

---

# Permutation

A **permutation** counts arrangements where **order matters**.

If $$n$$ distinct objects are arranged, the number of possible arrangements is

$$
\boxed{n!}
$$

If some objects are identical, divide by the factorial of the number of repeated objects.

## Example

How many different signals can be formed using:

- 4 identical white flags,
- 3 identical red flags,
- 2 identical blue flags,

for a total of 9 flags arranged in a line?

The total number of arrangements is

$$
\boxed{
\frac{9!}{4!3!2!}
}
$$

$$
=
\boxed{1260}
$$

The denominator removes overcounting caused by identical flags.

---

# Combination

A **combination** counts the number of ways to choose $$r$$ objects from $$n$$ objects when **order does not matter**.

$$
\boxed{
\binom{n}{r}
=
\frac{n!}{(n-r)!r!}
}
$$

This is read as:

> "$$n$$ choose $$r$$"

---

## Example: Committee

A committee of 3 is chosen from 20 people.

Since order does not matter,

$$
\binom{20}{3}
=
\frac{20\cdot19\cdot18}{3\cdot2\cdot1}
=
\boxed{1140}
$$

possible committees.

---

## Special Cases

$$
\boxed{
\binom{n}{0}=1
}
$$

There is exactly one way to choose no objects.

$$
\boxed{
\binom{n}{n}=1
}
$$

There is exactly one way to choose all $$n$$ objects.

By convention,

$$
\boxed{
\binom{n}{r}=0
\quad\text{if }r>n\text{ or }r<0
}
$$

---

## Combination vs. Permutation

Ask:

> Does changing the order create a different outcome?

- If **yes** → permutation 
- If **no** → combination

Example:

$$
ABC
$$

and

$$
CBA
$$

are different permutations, but they represent the same combination:

$$
\{A,B,C\}
$$

---

## Connection to the Binomial Theorem

The **binomial theorem uses combinations as its coefficients**: $\binom{n}{r}$ counts how many ways $r$ terms can be chosen from $n$ factors.

In ECE 203, this is important because the same counting idea appears in probability problems. 