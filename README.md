# Biometric Based Payment System

## Project Overview
The Biometric Based Payment System is designed to provide a secure and convenient payment method using biometric authentication. The system employs a fingerprint sensor for user identification, a 4x4 keypad for versatile input, and a 1.3” OLED display for clear feedback. An ESP32 microcontroller ensures secure handling of sensitive information with SHA-256 encryption. The system is supported by a centralized MySQL database and a web interface for managing payment history.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Contributing](#contributing)
- [Contact](#contact)

## Features
- Secure biometric authentication using fingerprint sensor
- Robust SHA-256 encryption for data protection
- Real-time transaction feedback via OLED display
- Versatile input options with a 4x4 keypad
- Centralized MySQL database for transaction data
- Web interface for managing payment history

## Installation

### Hardware Setup
1. **ESP32 Microcontroller**: Connect the ESP32 microcontroller to your system.
2. **R307 Fingerprint Sensor**: Interface the R307 fingerprint sensor with the ESP32.
3. **1.3” OLED Display**: Connect the OLED display to the ESP32.
4. **4x4 Matrix Keypad**: Interface the keypad with the ESP32.
5. **Power Supply**: Ensure the system is powered appropriately, using an 18650 Li-ion battery or an alternative power source.

### Software Setup
1. **Arduino IDE**: Download and install the Arduino IDE from [Arduino's official website](https://www.arduino.cc/en/Main/Software).
2. **ESP32 Board Configuration**: Add the ESP32 board configuration to the Arduino IDE by following the [instructions here](https://github.com/espressif/arduino-esp32).
3. **Required Libraries**:
   - Adafruit GFX Library
   - Adafruit SSD1306
   - ArduinoJson
   - Fingerprint Sensor Library for R307
4. **Server Setup**:
   - Install Apache server and MySQL database.
   - Configure the database with the necessary tables for transaction data.
   - Deploy the web interface for managing payment history.

## Usage
1. **Enrolment Mode**:
   - Register users' fingerprints by enrolling their biometric data into the system.
2. **Payment Mode**:
   - Users can access their wallets using their fingerprints.
   - Available options include checking balance, adding money, and making payments.
   - The system confirms transactions via the OLED display.

## Hardware Requirements
- ESP32 Microcontroller
- R307 Fingerprint Sensor
- 1.3” OLED Display
- 4x4 Matrix Keypad
- Power Supply (18650 Li-ion Battery or equivalent)

## Software Requirements
- Arduino IDE
- Apache Server
- MySQL Database
- PHP
- HTML/CSS/JavaScript for web interface

## Contributing
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/AmazingFeature`).
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4. Push to the branch (`git push origin feature/AmazingFeature`).
5. Open a Pull Request.

## Contact
Project Associates:
- S Suhas
- Shreyas P
- Vyshnavi H K
- Chitra A
