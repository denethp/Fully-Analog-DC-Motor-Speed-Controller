# Fully Analog PID DC Motor Speed Controller

> Fully analog closed-loop DC motor speed controller featuring analog PID control, custom PWM generation, and frequency-to-voltage feedback without using any microcontroller or digital signal processing.

<p align="center">

<a href="https://canva.link/gsjmjxzgy5exvvy">
<img src="https://img.shields.io/badge/Project_Presentation-View_on_Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white">
</a>

</p>

---

## Project Overview

This project demonstrates the design and implementation of a **fully analog closed-loop control system** capable of regulating the speed of a DC motor entirely using analog electronics.

Unlike conventional motor controllers that rely on microcontrollers or digital PID algorithms, every stage of this controller—from feedback acquisition to PWM generation—is implemented using operational amplifiers, passive components, and discrete power electronics.

The complete control loop consists of:

- Analog Frequency-to-Voltage Converter
- Analog PID Controller
- Analog PWM Generator
- MOSFET Power Driver

No microcontrollers, DSPs, FPGAs, or digital control algorithms are used.

---

## Features

- Fully analog closed-loop speed control
- Analog PID controller (P + I + D)
- Custom Frequency-to-Voltage Converter
- Analog PWM generation using triangular wave comparison
- Schmitt Trigger based oscillator
- Precision rectifier and voltage clipper
- IRLZ44N MOSFET motor driver
- Real-time continuous feedback
- Designed and tested entirely on hardware

---

## Control System Architecture

```text
          Reference Speed
                 │
                 ▼
        Error Calculation
                 │
                 ▼
        Analog PID Controller
                 │
                 ▼
     Analog PWM Signal Generator
                 │
                 ▼
      MOSFET Power Amplifier
                 │
                 ▼
             DC Motor
                 │
         Encoder Feedback
                 │
                 ▼
   Frequency-to-Voltage Converter
                 │
                 └───────────────► Feedback
```

---

## Hardware Modules

### Frequency-to-Voltage Converter

Converts encoder pulse frequency into a proportional analog voltage using:

- RC Low-pass Filter
- Peak Detector
- Analog Signal Conditioning

---

### Analog PID Controller

Implements

- Proportional
- Integral
- Derivative

control entirely using operational amplifier circuits.

---

### Analog PWM Generator

Generates PWM through

- Schmitt Trigger Oscillator
- Integrator
- Voltage Comparator
- Precision Rectifier
- Positive Clipper

to produce a clean 0–5 V PWM signal.

---

### MOSFET Driver Stage

Uses an **IRLZ44N** logic-level MOSFET with

- Gate resistor
- Pull-down resistor
- Schottky flyback diode
- Decoupling capacitor

for efficient and reliable motor driving.

---

## Components

| Category | Components |
|-----------|------------|
| Operational Amplifier | TL072 |
| MOSFET | IRLZ44N |
| Flyback Diode | 1N5819 |
| Signal Diode | 1N4148 |
| Passive Components | Resistors, Capacitors, Potentiometers |

---

## Experimental Results

The completed system successfully demonstrated

- Stable closed-loop motor speed regulation
- Continuous analog feedback
- Effective PID tuning
- Smooth PWM control
- Reliable hardware implementation

Experimental observations verified the expected behavior of proportional, integral, and derivative control actions.

---

## Repository Structure

```text
.
├── Report/
├── Simulations/
├── Hardware/
├── Images/
└── README.md
```

---

## Technologies

- Analog Electronics
- Control Systems
- PID Control
- PWM Generation
- Power Electronics
- Operational Amplifiers
- Motor Control

---

## Team

**Team Neural Nexus**

- Deneth Priyadarshana
- Lasan Perera
- Isitha Dinujaya
- Dulana Pitiwaduge

Department of Electronic & Telecommunication Engineering

University of Moratuwa

---

## Project Presentation

📽️ **Presentation Slides**

https://canva.link/gsjmjxzgy5exvvy

---

## License

This project was developed for academic purposes as part of the EN2160 Analog Electronics module at the University of Moratuwa.
