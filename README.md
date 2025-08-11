
# Wide-Range Low-Distortion Sine-Wave Generator

## Overview
This project implements a **wide-range, low-distortion sine-wave generator** designed for laboratory use, targeting applications such as audio equipment testing, filter characterization, sensor calibration, and data acquisition systems.  
It combines a **Wien-Bridge Oscillator (WBO)** for low-distortion sine generation with a **Class-AB push-pull amplifier** for efficient, high-fidelity output.

Developed as part of **EN2111 – Electronic Circuit Design** at the **University of Moratuwa**.

---

##  Design Goals & Specifications
| Parameter                 | Target Value                  |
|---------------------------|--------------------------------|
| Frequency range           | 20 Hz – 20 kHz (continuously tunable) |
| Output amplitude          | 1 Vpp – 5 Vpp                  |
| Load capability           | 1 kΩ – 8 Ω                     |
| Total harmonic distortion | ≤ 1%                           |
| Power rails               | ±15 V                          |

---

##  System Architecture
1. **Stage 1 – Wien-Bridge Oscillator**
   - Low intrinsic distortion sine-wave generator
   - Ganged potentiometer for simultaneous frequency & gain adjustment
   - Maintains amplitude stability across the tuning range

2. **Stage 2 – Class-AB Amplifier**
   - Complementary emitter-follower design (TIP31AG/TIP32AG)
   - Drives low-impedance loads with minimal crossover distortion
   - VBE-multiplier biasing for improved linearity

---

## Key Design Highlights
- **Frequency Tuning:** 18.5 Hz – 19.58 kHz achieved with Rmin ≈ 82 Ω, Rmax ≈ 100 kΩ, C = 0.1 μF.
- **Gain Control:** Adjustable Class-AB gain (0.8 – 5.3) via R5.
- **Low THD:** Measured THD ≈ 0.41% at 1.25 kHz and ≈ 0.59% at 125 Hz.
- **Load Performance:** Stable output across 8 Ω to 1 kΩ loads.

---

##  Simulation & Verification
### Simulation Tools:
- **Proteus** – Wien-Bridge Oscillator design validation
- **Multisim** – Class-AB amplifier performance analysis

### Hardware Testing:
- Oscilloscope & dummy load verification
- Frequency and amplitude measurements match theoretical values within ±5%
- FFT analysis confirms THD < 1%

---

##  Component Selection
- **Op-Amp:** TL072 – low noise, high slew rate, wide bandwidth
- **Output Transistors:** TIP31AG/TIP32AG – robust push-pull pair
- **Biasing Diodes:** 1N4148 – temperature-stable forward voltage
- **Driver Transistor:** 2N3904 – suitable for preamp stage current requirements
- **Ganged Potentiometer:** Ensures matched R1 & R2 for stable tuning

---


