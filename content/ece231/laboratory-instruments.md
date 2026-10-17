---
title: "Laboratory Instruments"
---

## What I learned

This lab introduced the function generator, oscilloscope, and digital multimeter (DMM). The main lesson was to check **what quantity an instrument reports** and **how its settings affect the reading** before comparing measurements.

### Function generator: 50 Ω and High-Z settings

The function generator has an internal 50 Ω output resistance. Its displayed amplitude assumes the load setting selected on the generator.

With our high-impedance oscilloscope input, the measured peak-to-peak voltages were approximately twice as large when the generator was set to **50 Ω** as when it was set to **High-Z**. For example, the sine wave measured about **10.2 Vpp** in the 50 Ω setting and **5.07 Vpp** in High-Z.

**Remember:** Check both the generator’s load setting and the impedance of the instrument or circuit connected to it. A “50 Ω” generator setting does not mean the oscilloscope input is a 50 Ω load.

### Oscilloscope: reading a waveform

- **Vertical scale (V/div)** sets how much voltage each vertical division represents.
- **Horizontal scale (s/div)** sets how much time each horizontal division represents.
- Estimate peak-to-peak voltage by multiplying the waveform’s vertical span in divisions by V/div.
- Cursors let me measure between two selected points; automatic measurements calculate values from the captured waveform.
- Triggering starts acquisitions at a chosen voltage crossing and edge direction, making a repeating waveform appear stable.
- Keep the same scale settings when saving waveforms that I want to compare visually.

For our square wave, the automatic peak-to-peak reading was higher than the cursor reading. The automatic measurement included overshoot or undershoot, while we placed the cursors near the usual high and low levels.

### DMM: AC voltage means RMS voltage

The DMM’s AC voltage reading is an **RMS value**, whereas our earlier oscilloscope tables recorded **peak-to-peak voltage**. I should convert them to the same quantity before comparing them.

| Zero-offset waveform | RMS voltage from peak-to-peak voltage |
| --- | --- |
| Sine | $V_{\mathrm{RMS}}=\dfrac{V_{\mathrm{pp}}}{2\sqrt{2}}$ |
| Square | $V_{\mathrm{RMS}}=\dfrac{V_{\mathrm{pp}}}{2}$ |
| Symmetric ramp/triangle | $V_{\mathrm{RMS}}=\dfrac{V_{\mathrm{pp}}}{2\sqrt{3}}$ |

Our DMM readings agreed closely with these calculations: **1.768 V** for the 5 Vpp sine, **1.998 V** for the 4 Vpp square, and **0.863 V** for the 3 Vpp ramp. This shows why I cannot use the sine-wave RMS formula for every waveform.

Setting the ramp’s **symmetry to 50%** produces a triangle wave.

### Frequency and measurement limits

When we tripled the waveform frequencies, the DMM readings changed only slightly. For example, the ramp reading changed from **0.863 V to 0.856 V**. At frequencies beyond an instrument’s specified bandwidth, its reading may become inaccurate, so I should check its frequency range rather than assume every AC reading is reliable.

## Checklist for the next lab

1. Check the function generator’s waveform, frequency, amplitude, offset, and load setting.
2. Check the oscilloscope’s probe setting, V/div, s/div, and trigger.
3. Check whether a displayed voltage is **peak**, **peak-to-peak**, or **RMS**.
4. On the DMM, select **AC voltage** when measuring the RMS voltage of an AC waveform.
5. Before connecting leads, check the ground connection: the outer conductor of the oscilloscope’s BNC input is earth-grounded.