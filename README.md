# High-Voltage Amplification of Trigger Signals

This repository contains a hardware project designed for fast response to low-voltage trigger signals and the output of high-voltage AC signals, primarily intended for dielectrophoresis cell screening and other related applications. The project leverages the STM32 microcontroller to generate square waves for gate driver control and communicate with the Human-Machine Interface (HMI) module.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Design Overview](#design-overview)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Dielectrophoresis is a technique used in various scientific and industrial applications to manipulate and separate particles based on their polarizability when subjected to non-uniform electric fields. This repository houses a hardware solution designed to efficiently and rapidly respond to low-voltage trigger signals, generating high-voltage AC signals for dielectrophoresis cell screening, and potentially other scenarios requiring similar functionality.

## Features

- **Fast Response:** The system is optimized for rapid response to low-voltage trigger signals, minimizing delay in generating high-voltage AC signals.

- **Wide Trigger Signal Support:** This hardware supports trigger signal inputs ranging from 3.3V to 5V, making it compatible with various source devices.

- **Voltage Adjustment via HMI:** Output voltage can be adjusted within the range of approximately 80V to 800V through the Human-Machine Interface (HMI) interface, providing flexibility for different applications.

- **Low Transmission Delay:** The typical transmission delay for this system is around 100ns, ensuring minimal time lag between input trigger signals and high-voltage AC signal output.

- **STM32 Microcontroller:** The project utilizes the STM32 microcontroller for multiple key functions:
  - Generating square waves for the gate driver.
  - Communication with the HMI module to enable user interaction and control.

- **Slave Gating Mode:** The STM32 timer operates in slave gating mode, enhancing synchronization and precision in signal generation.

- **Trigger Signal Control:** The default state of the trigger signal is pulled up. It can be triggered by:
  - An external input low-level signal.
  - Activation of the pull-down MOSFET via the HMI module.

- **Hardware Timer Utilization:** The trigger signal is directly applied to the hardware timer without relying on STM32 arithmetic control, ensuring minimal signal processing delay.

- **Low Propagation Delay:** Both the gate driver and MOSFETs are carefully selected for their low propagation delay characteristics, guaranteeing the rapid response required for dielectrophoresis applications.

## Design Overview

The hardware design of this project focuses on efficiently amplifying trigger signals to produce high-voltage AC signals for dielectrophoresis cell screening. The core components and design principles include:

- **STM32 Microcontroller:** This microcontroller serves as the brain of the system, generating square waves for the gate driver and facilitating communication with the HMI module.

- **Gate Driver:** The gate driver is responsible for controlling the switching of MOSFETs in response to trigger signals, ensuring precise and rapid signal amplification.

- **MOSFETs:** The project incorporates MOSFETs with low propagation delay characteristics to minimize signal processing time and enable fast response to trigger signals.

- **HMI Module:** The Human-Machine Interface (HMI) module allows users to interact with and control the system, including triggering the signal and adjusting various parameters.

## Usage

To use this hardware project effectively, follow these steps:

1. **Clone the Repository:** Clone this GitHub repository to your local machine.

2. **Hardware Setup:** Assemble the required hardware components as per the design specifications and wiring instructions provided in the repository.

3. **STM32 Configuration:** Configure the STM32 microcontroller to generate square waves for the gate driver and establish communication with the HMI module.

4. **Trigger Signal Control:** Understand how to control the trigger signal using either external input or the HMI module, depending on your application requirements.

5. **Voltage Adjustment:** Utilize the HMI interface to adjust the output voltage according to your specific needs, within the range of approximately 80V to 800V.

6. **Power Up:** Power up the system and ensure that it operates as intended.

For detailed usage instructions and code examples, refer to the documentation and code within the repository.

## Contributing

Contributions to this project are welcome! If you have improvements, bug fixes, or new features to propose, please submit a pull request. For major changes, it's recommended to discuss your ideas first by opening an issue.

## License

This project is licensed under the [MIT License](LICENSE), which means you are free to use, modify, and distribute the code for both commercial and non-commercial purposes. Please review the full license for more details.
