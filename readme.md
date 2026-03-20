# Battery-Powered ESP32 Environmental Sensor Node

## Overview

This project is a compact, battery-powered environmental monitoring device built around the ESP32. It is designed to measure temperature, humidity, and atmospheric pressure, and transmit data wirelessly over Wi-Fi.

The system integrates power management, battery charging, sensing, and communication into a single PCB, making it suitable for IoT applications and embedded product prototyping.

---

## Features

* ESP32-based Wi-Fi connectivity
* Environmental sensing (temperature, humidity, pressure)
* Battery-powered operation (Li-Po)
* USB-C power input and charging
* Integrated battery protection
* Low-power design (deep sleep capable)
* UART interface for programming and debugging

---

## Hardware Architecture

The system is composed of the following main subsystems:

### Power Subsystem

* USB-C 5V input
* Li-Po battery charging IC
* Battery protection circuit
* 3.3V regulation stage
* Bulk and decoupling capacitors

### Processing Unit

* ESP32-WROOM-32 module
* Boot configuration and reset circuitry
* UART programming interface

### Sensor Subsystem

* BME280 environmental sensor (I2C interface)
* Pull-up resistors for I2C communication

---

## Block Diagram

```
USB-C → Charger → Battery → Regulator → ESP32 → Sensor (I2C)
```

---

## Design Highlights

* Modular schematic organization (power / MCU / sensor)
* Proper decoupling and power distribution
* ESP32 antenna keep-out respected
* I2C bus design with pull-up resistors
* Battery protection and safe charging design

---

## Key Engineering Decisions

* **ESP32 Module Selection**
  Used a pre-certified ESP32 module to simplify RF design and ensure reliable Wi-Fi performance.

* **Battery-Powered Architecture**
  Designed around a single-cell Li-Po battery for portability and real-world IoT use cases.

* **Power Regulation Strategy**
  Implemented a regulated 3.3V rail to ensure stable operation during ESP32 current spikes.

* **USB-C Power-Only Configuration**
  USB-C connector used strictly for power input, avoiding unnecessary USB data complexity.

* **I2C Sensor Interface**
  Selected a digital sensor with I2C to minimize pin usage and simplify routing.

---

## PCB Design

* 2-layer PCB
* Ground plane for signal integrity
* Compact component placement
* Standard SMD components (0603 passives)
* Connector placement optimized for usability

---

## Files Included

### Design Files

* Schematic files
* PCB layout files

### Manufacturing Files

* Gerbers
* Drill files
* Bill of Materials (BOM)
* Pick-and-place files

### Documentation

* Block diagram
* Rendered board images

---

## Applications

* IoT environmental monitoring
* Smart home systems
* Remote sensing nodes
* Battery-powered embedded systems

---

## Future Improvements

* Power path optimization (load sharing / advanced charger IC)
* Lower power consumption tuning
* OTA firmware update support
* Enclosure design integration
* Additional sensor support

---

## Author

Hardware design and layout by Abdelwahed Eloued

---

## License

This project is open-source and available under the MIT License.
