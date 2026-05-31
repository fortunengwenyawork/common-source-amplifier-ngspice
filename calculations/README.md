Common-Source NMOS Amplifier Design Calculations

Overview

This document summarizes the analytical calculations and simulation results obtained during the design and verification of a Common-Source NMOS Amplifier using KiCad and ngspice.

The purpose of this analysis was to establish a stable operating point, verify transistor bias conditions, and evaluate circuit behavior through transient and DC operating-point simulations.

⸻

Circuit Parameters

Component	Value
Supply Voltage (VDD)	12 V
Drain Resistor (R1)	4.7 kΩ
Source Resistor (R4)	1 kΩ
Gate Bias Resistor (R2)	1 MΩ
Gate Bias Resistor (R3)	1 MΩ
Load Resistor (R5)	100 kΩ
Input Capacitor (C1)	10 µF
Output Capacitor (C2)	10 µF
Input Signal	100 mV @ 1 kHz

⸻

Gate Bias Calculation

The gate voltage is established using a voltage-divider network.

Formula

VG = VDD × (R2 / (R2 + R3))

Substitution

VG = 12 × (1M / (1M + 1M))

Result

VG = 6.0 V

⸻

Operating Point Results

Measured directly from ngspice operating-point analysis.

Parameter	Measured Value
Gate Voltage (VG)	6.0 V
Source Voltage (VS)	2.11 V
Drain Voltage (VD)	2.11 V
Drain Current (ID)	≈ 2.11 mA

⸻

Drain Current Calculation

Using the source resistor and Ohm’s Law:

ID ≈ IS

ID = VS / RS

ID = 2.11 / 1000

ID = 2.11 mA

⸻

Source Voltage Verification

Voltage drop across the source resistor:

VRS = ID × RS

VRS = 2.11 mA × 1 kΩ

VRS = 2.11 V

This matches the simulated source voltage.

⸻

Drain Resistor Voltage Drop

VRD = ID × RD

VRD = 2.11 mA × 4.7 kΩ

VRD = 9.92 V

⸻

Gate-to-Source Voltage

VGS = VG − VS

VGS = 6.0 − 2.11

VGS = 3.89 V

This value places the transistor in a conducting region.

⸻

Input Signal

Applied input waveform:

Vin(t) = 0.1 sin(2π1000t)

Where:

* Amplitude = 100 mV
* Frequency = 1 kHz

⸻

Capacitor Functions

Input Coupling Capacitor (C1)

Purpose:

* Blocks DC voltage from the signal source
* Passes AC input signal to the gate

Output Coupling Capacitor (C2)

Purpose:

* Blocks DC bias from the drain
* Passes AC signal to the load resistor

⸻

Engineering Observations

* The gate divider successfully established a 6 V bias voltage.
* Source degeneration provided operating-point stability.
* Transient analysis verified proper waveform generation.
* Operating-point analysis confirmed transistor conduction.
* Simulation setup was successfully implemented using KiCad and ngspice.
* A model-related limitation prevented verification of voltage gain, highlighting the importance of selecting realistic vendor-specific MOSFET models.

⸻

Skills Demonstrated

* Analog Circuit Design
* MOSFET Biasing Analysis
* KiCad Schematic Capture
* ngspice Simulation
* Operating Point Analysis
* Waveform Interpretation
* Circuit Debugging
* Technical Documentation

⸻

Conclusion

The project successfully demonstrated the complete workflow of designing, simulating, and analyzing a Common-Source NMOS amplifier. Through transient and operating-point simulations, the circuit bias conditions were verified and documented. The project provided practical experience with analog circuit design, SPICE-based simulation, and engineering troubleshooting methodologies commonly used in industry.
