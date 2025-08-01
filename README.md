# High-Speed Dynamic Latch Comparator (gpdk090)

This project implements a high-speed CMOS dynamic latch comparator using the gpdk090 process in Cadence Virtuoso. It is suitable for use in low-power, moderate-to-high-speed applications such as ADCs, decision circuits, or zero-crossing detectors.

## Features

Technology Node: gpdk090 (90 nm)  
Minimum Transistor Width: 100 nm (0.10 µm)  
Clocked Dynamic Operation  
Regenerative Positive Feedback for Fast Decision  
Fully Differential Input (INP/INN)  
Low Power Operation  
Designed and Simulated in Cadence Virtuoso (Spectre)

## Schematic Overview

The comparator uses:  
- A differential input pair  
- Clocked tail current source (NMOS switch)  
- Cross-coupled inverters (positive feedback latch)  
- Optional reset circuit (PMOS shorting outputs)

## Transistor Sizing Summary*

| Block                      | Transistors | W (µm) | L (µm) | Fingers |
|---------------------------|-------------|--------|--------|---------|
| Differential Input Pair   | M1, M2      | 0.36   | 0.12   | 3       |
| Cross-Coupled Inverters   | M3–M6       | 0.24   | 0.09   | 2       |
| Tail NMOS (clocked)       | M7          | 0.48   | 0.09   | 4       |
| Reset PMOS (optional)     | M8          | 0.24   | 0.09   | 2       |

## Simulation Setup

Simulator: Spectre (Cadence ADE)  
Supply Voltage (VDD): 1.2 V  
Clock Source (CLK): 100 MHz square wave (vsource)  
Inputs (INP, INN): vsin sources  
- Frequency: 10 MHz  
- Amplitude: 0.2 V ± offset (to test input resolution)  
Testbench Configuration: transient simulation for approximately 100 ns

## Simulation Goals

- Validate high-speed decision time  
- Observe regeneration behavior  
- Measure input-referred offset  
- Estimate power consumption (optional)

## Output Waveform Example

The output shows successful latching of comparator state based on INP vs INN at the clock edge.

You can include a waveform image here once available.

## Repository Structure

*Sizing is still under work due to DRC limitations of GPDK090.

