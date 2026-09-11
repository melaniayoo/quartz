---
title: Pole and Zero
---

**Poles** and **zeros** describe how a circuit or system responds to different frequencies.

They come from the system's transfer function.

# Transfer Function

A transfer function can be written as:

$$
H(s)=\frac{\text{Numerator}}{\text{Denominator}}
$$

# Zero

A **zero** is a value of (s) that makes the transfer function equal to zero.

Zeros come from the **numerator**.

```text id="pz1"
Numerator = 0
    ↓
   Zero
```

A zero usually causes the magnitude response to increase in slope.

For a simple first-order zero:

* magnitude slope changes by about **+20 dB/decade**
* phase can increase by about **+90°**

# Pole

A **pole** is a value of (s) that makes the denominator equal to zero.

Poles come from the **denominator**.

```text id="pz2"
Denominator = 0
      ↓
     Pole
```

A pole usually causes the magnitude response to decrease in slope.

For a simple first-order pole:

* magnitude slope changes by about **−20 dB/decade**
* phase can decrease by about **−90°**

# Example

For:

$$
H(s)=\frac{1+s/\omega_z}{1+s/\omega_p}
$$

* (\omega_z) → zero frequency
* (\omega_p) → pole frequency

The pole and zero change the shape of the [[Bode Plot]].

# Pole vs. Zero

| Pole                          | Zero                           |
| ----------------------------- | ------------------------------ |
| Comes from denominator        | Comes from numerator           |
| Usually decreases gain slope  | Usually increases gain slope   |
| Adds phase lag                | Adds phase lead                |
| Can affect stability strongly | Can improve or worsen response |

# Stability

Poles are especially important for [[Feedback System|feedback systems]].

If poles are located in unstable regions, the system can oscillate or become unstable.

Poles and zeros also affect:

* bandwidth
* [[Phase Margin]]
* frequency response
* transient response

# Key Idea

**Pole → tends to reduce gain and add phase lag.**

**Zero → tends to increase gain and add phase lead.**

Poles and zeros determine the shape and stability of a system's frequency response.
