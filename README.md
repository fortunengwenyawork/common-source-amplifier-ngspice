Common Source Amplifier Using NGspice

Overview

This project explores the design and analysis of a MOSFET common-source amplifier using NGspice. The common-source amplifier is one of the most fundamental analog circuit topologies and serves as a building block for larger analog and mixed-signal integrated circuits.

The purpose of this project is to develop a deeper understanding of transistor-level analog design through simulation and analysis of amplifier behavior under DC, AC, and transient operating conditions.

Objectives

* Design a functional NMOS common-source amplifier
* Establish a stable transistor bias point
* Analyze DC operating conditions
* Measure small-signal voltage gain
* Evaluate frequency response
* Investigate transient response to sinusoidal inputs
* Gain experience using NGspice for analog circuit simulation

Tools Used

* NGspice
* GitHub
* Markdown Documentation

Circuit Description

The amplifier consists of a single NMOS transistor operating in a common-source configuration. A drain resistor converts variations in drain current into amplified voltage variations at the output.

The circuit includes:

* NMOS transistor
* Drain resistor
* Gate bias network
* Input signal source
* DC power supply

Simulations Performed

DC Operating Point Analysis

The DC operating point analysis is used to determine:

* Gate voltage
* Drain voltage
* Source voltage
* Drain current
* Transistor operating region

Transient Analysis

Transient simulations are performed to evaluate the amplifier response to a time-varying input signal and verify voltage amplification.

AC Small-Signal Analysis

AC analysis is used to determine:

* Voltage gain
* Frequency response
* Bandwidth limitations

Engineering Concepts Demonstrated

* MOSFET operation
* Transistor biasing
* Small-signal analysis
* Voltage gain
* Frequency response
* Analog circuit design
* SPICE simulation workflows

Repository Structure

common-source-amplifier-ngspice/
│
├── README.md
│
├── netlists/
│   └── common_source_amplifier.cir
│
├── docs/
│   ├── dc_operating_point.png
│   ├── transient_response.png
│   ├── ac_response.png
│   └── project_report.md
│
└── calculations/
    └── design_calculations.md

Project Status

* Circuit Design
* DC Operating Point Analysis
* Transient Analysis
* AC Frequency Response Analysis
* Gain Calculation
* Documentation
* Final Report

Expected Results

The completed project will demonstrate the operation of a transistor-level voltage amplifier and provide quantitative measurements of gain, bandwidth, operating point, and transient behavior. The project will serve as an introduction to analog integrated circuit design principles using industry-standard SPICE simulation tools.

License

This project is released under the MIT License.
