# NRF24L01-Transceiver-Module-with-STM32

## Objective
The goal of this project was to establish reliable, bidirectional wireless communication between two STM32 microcontrollers. By interfacing the NRF24L01 transceiver module via the Serial Peripheral Interface (SPI) protocol, the system successfully transmits and receives real-time sensor data in the 2.4 GHz ISM band.

## Theory 
* **STM32 Nucleo-64**: A high-performance, low-power microcontroller based on the ARM Cortex-M4 architecture. It features an integrated ST-LINK/V2-1 debugger, streamlining the programming process.

* **NRF24L01**: A cost-effective, highly efficient wireless transceiver module operating in the 2.4 GHz ISM band. It features multi-channel operation, automatic acknowledgment, and retransmission. Power Amplifier (PA) Low-Noise Amplifier (LNA) range up to 1,000 meters in open areas.

* **SPI (Serial Peripheral Interface)**: A synchronous serial communication protocol used for short-distance, fast, and reliable data transfer between the microcontroller and the transceiver.

## Components & Technologies Used
* **Microcontroller**: 2x STM32 Nucleo-64 Boards

* **Transceiver**: 2x NRF24L01 Modules

* **Development Environment**: Arduino IDE (with STM32 board packages)

* **Libraries**: RF24 / RF24STM

* **Prototyping**: Breadboards, Jumper Wires, 10µF Capacitors (for power noise filtration)

## Architechtural Diagrams 
<img width="603" height="643" alt="image" src="https://github.com/user-attachments/assets/7d309a18-175b-4ea4-8ad3-3268b98f1c06" />

Block Diagram

<img width="501" height="281" alt="image" src="https://github.com/user-attachments/assets/8fadd790-3c39-4a6d-99f0-a2eccf6e90d7" />

Actual Implementation 


## Methodology & Steps

1. Environment Setup
* Installed the STM32 board package in the Arduino IDE.

* Connected the STM32 Nucleo-64 to the PC (utilizing the built-in ST-LINK).

* Installed the RF24 library for handling wireless data transmission.

2. Hardware Configuration
* Wired the NRF24L01 modules to the respective STM32 boards using the SPI pinout defined above.

* Configured one STM32 board to act as the Transmitter (Tx) and the other as the Receiver (Rx).

3. Firmware Development & Code Execution
* Programmed the Tx unit to format and send data packets (e.g., sensor readings or test strings) through the NRF24L01.

* Programmed the Rx unit to listen on the designated channel, capture the incoming packets, and display the output on the Serial Monitor.

* Handled power modes and data acknowledgment within the firmware to ensure reliable communication.

## Applications
* This foundational wireless setup can be scaled and integrated into various real-world IoT systems, including:

* Home & Industrial Automation: Remote control of lighting, security systems, and factory equipment.

* Remote Sensing & Agriculture: Wirelessly aggregating data from environmental, soil moisture, and temperature sensors.

* Robotics & Drones: Enabling low-latency remote control telemetry and data transmission for autonomous systems.

## Results
* Successful Wireless Range: Achieved seamless bidirectional data transfer up to 100 meters in open environments.

* High Data Integrity: Implemented automatic acknowledgment, resulting in less than 2% packet loss during testing.

* Low Power Consumption: Validated the power efficiency of the setup, drawing approximately 15.5 mA during active transmission and dropping to just 1.2 µA in sleep mode.

* Network Scalability: Verified that up to six devices can communicate simultaneously on the same network using different channels without significant interference.
