

# 🌐 LoRa Communication System with RFM95 and Arduino

This project demonstrates a simple communication system using LoRa modules (RFM95) with Arduino. The setup includes a master device that sends commands and receives data, and a slave device that responds to commands and sends acknowledgments. The communication happens at a frequency of 433.0 MHz.

## 📑 Table of Contents
- [📖 Overview](#overview)
- [🔧 Components](#components)
- [📊 Circuit Diagram](#circuit-diagram)
- [⚙️ Setup Instructions](#setup-instructions)
- [💻 Code Overview](#code-overview)
- [📝 Detailed Steps](#detailed-steps)
- [🛠️ Troubleshooting](#troubleshooting)
- [📄 License](#license)
- [💖 Donation](#donation)

## 📖 Overview
This project is designed to showcase basic communication between two LoRa-enabled devices using the RFM95 module. The master device sends a command, to which the slave device responds. The slave device also provides an acknowledgment of the received command.

### 🌟 Features
- **📡 Master Device**: Sends commands and receives responses.
- **🖥️ Slave Device**: Receives commands and sends acknowledgments and data.
- **📶 Communication Frequency**: 433.0 MHz.
- **✅ Acknowledgment Mechanism**: Ensures reliable communication.

## 🔧 Components
- **🔌 Arduino Boards**: Used as the microcontroller platform.
- **📡 RFM95 LoRa Modules**: For wireless communication.
- **📦 SPI Library**: To handle SPI communication.
- **📦 RH_RF95 Library**: To handle LoRa communication.
- **🔔 Buzzer**: Provides audible feedback on the slave device.

## 📊 Circuit Diagram
Include the circuit diagram here (replace this text with the actual diagram image).

## 🖼️ Scenario Diagram
![Scenario Diagram](Scenario%20(1).jpg)

## ⚙️ Setup Instructions

1. **Hardware Connections**:
   - Connect the RFM95 module to the Arduino as per the following pin definitions:
     - `RFM95_CS` to pin 26
     - `RFM95_RST` to pin 12
     - `RFM95_INT` to pin 25
   - Connect a buzzer to pin 2 on the slave Arduino.

2. **Software Setup**:
   - Install the necessary libraries:
     - [SPI](https://www.arduino.cc/en/Reference/SPI)
     - [RH_RF95](https://www.airspayce.com/mikem/arduino/RadioHead/classRH__RF95.html)
   - Clone the repository and load the provided master and slave device code onto the respective Arduino boards:
     ```bash
     git clone https://github.com/Esmail-Sarhadi/LoRa-Communication-System.git
     cd LoRa-Communication-System
     ```

3. **Operation**:
   - Power the Arduino boards.
   - Open the Serial Monitor at a baud rate of 115200 to view communication logs.
   - The master device will send commands periodically. The slave device will respond with data and acknowledgment.

## 💻 Code Overview

### Master Device
- **Initialization**: Sets up the LoRa module, configures the frequency, and sets the transmission power.
- **Loop**: Continuously sends a command and waits for a response. If no response is received within the timeout period, it resends the command. Upon receiving the correct response, it sends an acknowledgment.

### Slave Device
- **Initialization**: Sets up the LoRa module, configures the frequency, and sets the transmission power. Also initializes the buzzer.
- **Loop**: Continuously listens for incoming commands. Upon receiving a command, it checks the command type and sends the appropriate response or acknowledgment. The buzzer provides an audible indication when data is received.

## 📝 Detailed Steps

### Master Device Setup
1. Connect the RFM95 module to the master Arduino using the defined pins.
2. Load the master device code onto the Arduino.
3. Open the Serial Monitor to observe the sending of commands and receiving of responses.

### Slave Device Setup
1. Connect the RFM95 module and the buzzer to the slave Arduino using the defined pins.
2. Load the slave device code onto the Arduino.
3. Open the Serial Monitor to observe the receiving of commands and sending of responses.

## 🛠️ Troubleshooting
- **No Communication**: Ensure the wiring between the Arduino and the RFM95 module is correct.
- **Initialization Failed**: Check if the RFM95 module is correctly connected and powered.
- **No Response from Slave**: Ensure the slave device is powered and running the correct code.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 💖 Donation
If you found this project helpful, consider making a donation:

<a href="https://nowpayments.io/donation?api_key=REWCYVC-A1AMFK3-QNRS663-PKJSBD2&source=lk_donation&medium=referral" target="_blank">
     <img src="https://nowpayments.io/images/embeds/donation-button-black.svg" alt="Crypto donation button by NOWPayments">
</a>

