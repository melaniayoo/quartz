---
title: Comparator
---

A comparator is a circuit that compares two input voltages.

It has:

* a non-inverting input, `V+`
* an inverting input, `V−`
* one output

```text
If V+ > V− → output HIGH
If V+ < V− → output LOW
```

# How It Works

A comparator changes its output depending on which input voltage is greater.

```text
Sensor voltage ──→ V+
Reference voltage → V−
```

If the sensor voltage rises above the reference voltage, the output changes state.

# Example

Suppose:

```text
V+ = 3 V
V− = 2 V
```

Because `V+ > V−`, the output becomes HIGH.

If:

```text
V+ = 1 V
V− = 2 V
```

the output becomes LOW.

# Main Uses

Comparators are used for:

* threshold detection
* battery-level monitoring
* zero-crossing detection
* sensor interfaces
* converting analog signals into digital states
