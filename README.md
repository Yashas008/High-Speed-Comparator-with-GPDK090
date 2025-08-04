# High Speed CMOS Dynamic Comparator

## Problem Statement

Design a high speed dynamic latch comparator using CMOS technology that can reliably compare two differential input signals (INP and INN) and produce a valid digital output (OUTP, OUTN) synchronized to a clock edge. The comparator should operate at a supply of 1.2 V with minimal delay and sufficient gain to resolve small input differences (less than 10 mV), making it suitable for integration into high speed analog to digital converters (ADCs).

## Objective

Achieve fast decision time (less than 1 ns)  
Accurately distinguish input differences of 10 mV or less  
Output a valid logic level at each clock cycle  
Ensure regenerative positive feedback behavior  
Maintain correct polarity of output signals (OUTP equals 1 when INP greater than INN)

## Results Summary

Input Pair: Differential sinusoidal signals with amplitude ±0.2 V  
Clock: 100 MHz square wave  
Supply Voltage (VDD): 1.2 V  
Minimum detectable delta V (INP minus INN): Approximately 8 mV  
Latching Time: Approximately 300 ps  
Correct Output Polarity: Verified  
Regeneration Behavior: Confirmed  
Transient Simulation: Shows valid digital-level outputs switching in response to differential input and clock edges
Layout has been generated and vlaidated with DRC and LVS and parasitics have been extracted for said device.


### Output Snapshot

OUTP goes high when INP greater than INN at the rising clock edge  
OUTN goes high when INN greater than INP at the rising clock edge  
Latching behavior is consistent and repeatable

## Conclusion

The designed comparator meets the core requirements of high speed comparison. It successfully differentiates small input voltages at moderate clock speeds and demonstrates reliable positive feedback latching behavior. With further sizing refinement and layout symmetry, it is suitable for integration into medium to high speed ADC architectures.
