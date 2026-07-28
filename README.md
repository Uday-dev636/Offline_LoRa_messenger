# Offline_LoRa_messenger
A LoRa messenger allows offline communication using long-range LoRa modules

# LoRa Messenger using ESP32 and ESP8266

## Overview

This project is a simple LoRa-based messaging system built using an ESP32, an ESP8266, SX1278 (RA-02) LoRa modules, and SSD1306 OLED displays.

The main idea is to send a message from a mobile phone to an ESP32 through a web dashboard. The ESP32 then sends the message over LoRa to an ESP8266. The ESP8266 displays the received message on its OLED screen and also makes it available on its own web dashboard.

This project was developed to understand long-range wireless communication using LoRa and to build a lightweight messaging system without requiring an internet connection.

---

## Features

- Send messages from a mobile phone using a web dashboard.
- Long-range communication using LoRa (SX1278).
- OLED display shows sent and received messages.
- ESP32 and ESP8266 both create their own Wi-Fi Access Point.
- Simple web interface that works on any smartphone.
- Stable communication after updating the hardware connections and improving the code.

---

## Hardware Used

### Sender

- ESP32 Development Board
- SX1278 (RA-02) LoRa Module
- SSD1306 128×64 OLED Display

### Receiver

- NodeMCU ESP8266
- SX1278 (RA-02) LoRa Module
- SSD1306 128×64 OLED Display

---

## ESP32 Connections

### LoRa Module

| LoRa Pin | ESP32 Pin |
|----------|-----------|
| VCC | 3.3V |
| GND | GND |
| SCK | GPIO18 |
| MISO | GPIO19 |
| MOSI | GPIO23 |
| NSS (CS) | GPIO5 |
| RST | GPIO14 |
| DIO0 | GPIO2 |

### OLED Display

| OLED Pin | ESP32 Pin |
|----------|-----------|
| VCC | 3.3V |
| GND | GND |
| SDA | GPIO21 |
| SCL | GPIO22 |

---

## ESP8266 Connections

### LoRa Module

| LoRa Pin | ESP8266 Pin |
|----------|-------------|
| VCC | 3.3V |
| GND | GND |
| SCK | D5 |
| MISO | D6 |
| MOSI | D7 |
| NSS (CS) | D8 |
| RST | D1 |
| DIO0 | D2 |

### OLED Display

| OLED Pin | ESP8266 Pin |
|----------|-------------|
| VCC | 3.3V |
| GND | GND |
| SDA | D3 |
| SCL | D4 |

---

## Required Libraries

Install the following libraries using the Arduino Library Manager:

- LoRa by Sandeep Mistry
- Adafruit GFX Library
- Adafruit SSD1306 Library

Also install the latest board packages for:

- ESP32
- ESP8266

---

## How It Works

1. Connect your phone to the Wi-Fi hotspot created by the ESP32.
2. Open the sender dashboard in your browser.
3. Type a message and press **Send**.
4. The message is shown on the ESP32 OLED display.
5. The ESP32 transmits the message through the SX1278 LoRa module.
6. The ESP8266 receives the message.
7. The received message is displayed on its OLED screen.
8. Connect another phone to the ESP8266 hotspot to view the latest received message through its web dashboard.

---

## Changes Made

The original version of this project was modified and improved during testing.

Changes include:

- Updated LoRa pin connections.
- Corrected OLED wiring.
- Improved initialization process.
- Fixed communication issues between ESP32 and ESP8266.
- Added better error handling during startup.
- Cleaned up and optimized the source code.
- Improved overall stability after multiple hardware tests.

These changes helped make the communication more reliable and easier to use.

---

## Future Improvements

Some features that can be added in future versions:

- Two-way messaging
- Delivery acknowledgment (ACK)
- Message history
- Signal strength (RSSI) display
- Battery monitoring
- Time stamps
- Multiple LoRa nodes
- Password-protected web dashboard

---

## Project Images

You can add photos of:

- ESP32 Sender Setup
- ESP8266 Receiver Setup
- OLED Displays
- Web Dashboard
- Complete Hardware Connections

---

## Author

**Abhi**

B.Tech - Electronics and Communication Engineering

Andhra University

---

If you found this project useful, feel free to fork it, improve it, or use it for your own learning.
