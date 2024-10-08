# Biometric-Based Payment System

## Overview

The Biometric-Based Payment System is an advanced security and payment solution that leverages fingerprint recognition to facilitate secure transactions. This system integrates various components including a fingerprint sensor, a keypad for additional user inputs, an OLED display for visual feedback, and WiFi connectivity for network communication.

This project is implemented on the ESP32 microcontroller, utilizing the Adafruit Fingerprint sensor library for fingerprint recognition, and the Adafruit SSD1306 library for driving the OLED display. The system also features a simple web server to manage user accounts and perform transactions.

## Features

- **Fingerprint Authentication**: Securely authenticate users via fingerprint recognition.
- **User Management**: Manage user profiles including ID, name, balance, and role (admin/user).
- **Transaction Handling**: Perform balance checks and transactions securely.
- **OLED Display**: Provides visual feedback to users, including system status and instructions.
- **Keypad Interface**: Allows users to enter data and interact with the system.
- **WiFi Connectivity**: Connect to a network for online transactions and updates.
- **Password Hashing**: Securely hash user passwords using SHA-256 encryption with a fixed salt.

## Components

![image](https://github.com/user-attachments/assets/aeb31364-fa35-4358-80d1-f98ecdd799ce)

- **ESP32 S3 Microcontroller**: Main controller for the system.
- **Adafruit Fingerprint Sensor**: Captures and recognizes fingerprints.
- **Adafruit SSD1306 OLED Display**: Displays user interface and system messages.
- **4x4 Keypad**: Provides input for user interactions.

## Installation

1. **Hardware Setup**:
   - Connect the Adafruit Fingerprint sensor to the ESP32 using UART2 (TX to GPIO 12, RX to GPIO 1).
   - Connect the OLED display to the I2C pins (SDA to GPIO 17, SCL to GPIO 18).
   - Connect the Keypad:
      - Row Pins: Connect to GPIO pins 14, 13, 12, 11
      - Column Pins: Connect to GPIO pins 10, 9, 46, 3

2. **Software Setup**:
   - Install the Arduino IDE if you haven't already.
   - Add the ESP32 board to the Arduino IDE.
   - Install the required libraries:
     - `Adafruit Fingerprint Sensor Library`
     - `Adafruit SSD1306`
     - `Adafruit GFX`
     - `Keypad`
     - `AsyncTCP`
     - `ESPAsyncWebServer`
   - Clone or download the project repository to your local machine.
   - Open the project in the Arduino IDE and upload the code to the ESP32.

## Usage

1. **Setup WiFi**:
   - Ensure your ESP32 is connected to a WiFi network. Modify the `ssid` and `password` variables in the code if necessary.
2. **Add Users**:
   - Enroll fingerprints and set up user profiles using the fingerprint sensor and keypad interface.
3. **Perform Transactions**:
   - Use the keypad to initiate transactions and the OLED display to view transaction details and status.
4. **Access Web Server**:
   - Connect to the ESP32’s IP address via a web browser to manage user accounts and view transaction logs.

## Code Description

- **User Management**: Contains a `User` struct for managing user data and a global array for storing user profiles.
- **Fingerprint Authentication**: Uses the Adafruit Fingerprint library to capture and verify fingerprints.
- **Display Management**: Handles visual feedback through the Adafruit SSD1306 OLED display.
- **Web Server**: An asynchronous web server for managing users and transactions.
- **Password Hashing**: Implements SHA-256 hashing for secure password storage.
- **`hashPassword(const char *password)`**: Hashes passwords using SHA256 with a fixed salt.
- **`setup()`**: Initializes the hardware components, sets up the WiFi, and starts the web server.
- **`loop()`**: Handles fingerprint authentication and user interactions.

## Troubleshooting

- **Fingerprint Sensor Not Responding**: Check connections and ensure the sensor is properly initialized.
- **OLED Display Blank**: Verify connections and ensure the display is correctly configured.
- **Keypad Not Working**: Ensure proper wiring and verify pin assignments.

## Project Images

<p align="center">
  <img src="https://github.com/user-attachments/assets/89a0f944-5309-4a65-a491-6c0d29dfdac4" alt="Image 4" width="300"/>
  <img src="https://github.com/user-attachments/assets/d4783c38-d77e-45be-baac-9b118773b3f3" alt="Image 1" width="300"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/dbd4654a-9d40-439e-88f2-c98baac5379c" alt="Image 2" width="300"/>
  <img src="https://github.com/user-attachments/assets/9cf227ec-89d4-4b2c-a7d9-8323013086e3" alt="Image 3" width="300"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/44e26401-c8c0-403e-b905-8ae8128954a9" alt="Login Page" width="300"/>
  <img src="https://github.com/user-attachments/assets/3a30480b-b67d-42b7-80e5-b14fdfb2a980" alt="Admin Dashboard" width="300"/>
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/fa6092bc-2050-4ec9-9533-132fbc907339" alt="User Page" width="300"/>
</p>


## Contributing

Feel free to contribute to this project by submitting issues, suggestions, or improvements via GitHub.

## Acknowledgments

- Adafruit for providing the fingerprint sensor and OLED display libraries.
- The Arduino community for the open-source libraries and support.

For any additional questions or support, please contact [Shreyas P](mailto:shreyasp182002@gmail.com).
