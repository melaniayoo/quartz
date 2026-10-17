---
title: DRAM
---

DRAM stands for Dynamic Random Access Memory.
DRAM is commonly used as the main memory in computers and electronic devices.

# How It Works

Each DRAM cell stores one bit of data using:

* one transistor
* one capacitor

The capacitor gradually loses its electrical charge, so the data must be refreshed repeatedly.
This is why it is called dynamic memory.

It's beneficial to have many cells per unit area. In order to do that, we can make the distance between transistors narrower --> chip size gets smaller --> more chips on one wafer --> cost of production decreases --> price gets lower --> power consumption is reduced

# Main Uses

* computers
* smartphones
* servers
* graphics cards
* embedded systems

# Types of DRAM

## SDRAM

SDRAM stands for Synchronous Dynamic Random Access Memory.

It operates in synchronization with the system clock, which allows memory operations to be coordinated with the processor.

## DDR SDRAM

DDR stands for Double Data Rate.

It transfers data on both the rising and falling edges of the clock signal, allowing more data to be transferred per clock cycle.

Newer generations generally provide higher bandwidth and improved power efficiency.

## LPDDR

LPDDR stands for Low-Power Double Data Rate.

It is designed to consume less power than standard DDR memory.

It is commonly used in:

* smartphones
* tablets
* laptops
* mobile devices

## GDDR

GDDR stands for Graphics Double Data Rate.

It is designed for high-bandwidth graphics processing.

It is commonly used in:

* graphics cards
* gaming consoles
* GPUs

## HBM

HBM stands for High Bandwidth Memory.

It stacks multiple DRAM dies vertically and uses a very wide interface to transfer large amounts of data quickly.

HBM has become especially important because AI processors need extremely high memory bandwidth.
SK hynix, a Korean semiconductor company and a major HBM manufacturer, has gained significant market attention as demand for AI chips and HBM has increased.

It is commonly used in:

* high-performance GPUs
* AI accelerators
* supercomputers


# DRAM vs. SRAM

| DRAM                            | [[SRAM]]                    |
| ------------------------------- | --------------------------- |
| Uses a capacitor and transistor | Uses multiple transistors   |
| Requires refreshing             | Does not require refreshing |
| Slower                          | Faster                      |
| Higher capacity                 | Lower capacity              |
| Lower cost per bit              | Higher cost per bit         |
| Used as main memory             | Used mainly for cache       |
