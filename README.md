# Hi there, I'm Aakashdip Dey 👋

### ⚡ Hardware & PCB Design Engineer | Embedded Electronics & Mixed-Signal Circuits
📍 *Vellore, India* &nbsp;|&nbsp; 💼 *Specializing in High-Density Multilayer PCB Design, Analog Front-Ends & Power Systems*

[![Altium Designer](https://img.shields.io/badge/Altium%20Designer-25-brightgreen?style=flat-square&logo=altiumdesigner)](https://www.altium.com/)
[![PCB Design](https://img.shields.io/badge/PCB%20Design-4--Layer%20HDI%20%7C%20Controlled%20Impedance-blue?style=flat-square)](#-technical-competencies)
[![Mixed Signal](https://img.shields.io/badge/Circuits-Mixed--Signal%20%26%20Power%20Electronics-orange?style=flat-square)](#-technical-competencies)
[![GitHub Repos](https://img.shields.io/badge/Hardware%20Projects-Featured%20Designs-purple?style=flat-square)](#-featured-hardware-projects)

---

## 👨‍💻 About Me

I am a hardware design engineer dedicated to architecting robust, production-ready electronic systems from concept to fabrication. My work spans **multichannel mixed-signal acquisition boards**, **ultra-compact wearable IoT devices**, **high-speed processor development boards**, and **high-current electromechanical control platforms**.

* 🔭 **Core Focus:** Schematic capture, controlled-impedance multilayer PCB layout (Altium Designer), analog front-end (AFE) signal conditioning, power path management, and DFM/DFA compliance.
* 🛠️ **Fabrication Discipline:** Strict adherence to IPC-2221 design rules, zero-violation DRC checks, thermal relief optimization, and clean Gerber/BOM generation for seamless manufacturing.
* 🎯 **Goal:** Designing reliable hardware that bridges physical sensor instrumentation with connected edge computing.

---

## 🛠️ Technical Competencies

| Domain | Tools & Technologies |
|:---|:---|
| **EDA & CAD Software** | **Altium Designer**, Schematic Capture, 2-Layer & 4-Layer High-Density Layout, Rigid & FPC Interface Design, Footprint Creation (IPC-7351), Design Rule Checking (DRC), ODB++, Gerber RS-274X, NC Drill, Pick-and-Place Generation |
| **High-Speed & Signal Integrity** | 90Ω USB Differential Pair Routing (`DIFF90`), Controlled Impedance Stackups, Return Path Ground Plane Integrity, RF Antenna Layout & Keepouts (2.4GHz Wi-Fi / BLE), Crosstalk Suppression |
| **Mixed-Signal & Analog Front-End** | Precision Instrumentation Amplifiers (**TI INA333**), 16-Bit Delta-Sigma ADCs (**TI ADS1115** with PGA), 12-Bit DACs (**Microchip MCP4725**), Precision Shunt References (**LM4040**), Load Cell Amplifiers (**HX711**) |
| **Power Supply & Battery Management** | Switching Step-Down Buck Converters (**LM2596** with high-bulk transient filtering), Ultra-Low Noise Fast-Transient LDOs (**TI TL1963A**, **AP2112K**, **AMS1117**), Standalone Li-Ion/Li-Po Chargers (**Microchip MCP73831**), Automatic Ideal-Diode Power Path Switching (P-FET + Schottky) |
| **Circuit Protection & Reliability** | High-Energy TVS Diode Arrays (**Littelfuse AQ3045**, **SMAJ26CA** rated to ±30kV IEC 61000-4-2), Inductive Flyback Clamping, Inrush Current Damping, Reverse Polarity Protection |
| **Processors & Peripheral Interfaces** | **Espressif ESP32 & ESP32-S3** (Xtensa LX7 Dual-Core @ 240MHz), **FTDI USB Bridges** (FT231X), I2C, SPI, UART, USB Type-C (CC Configuration & USB-OTG/JTAG), PWM Motor Drivers |

---

## 🚀 Featured Hardware Projects

### 1. [ESP32-S3 High-Performance Development Board with Dual USB-C](https://github.com/AakashdipDey/esp32-s3-usbc-devkit)
*Custom 4-layer embedded development platform engineered for high reliability and noise-sensitive applications.*
* **Microcontroller:** Espressif ESP32-S3-MINI-1-N8 (Dual-Core 240MHz, 8MB Flash, Wi-Fi 4 / BLE 5.0).
* **Dual USB-C Topology:** One native USB-OTG/JTAG port plus an isolated **FTDI FT231XQ-R** USB-UART bridge port with automated transistor-based flashing (DTR/RTS cross-coupled SS8050 pair).
* **Power Distribution:** High-current **Texas Instruments TL1963A** 1.5A low-noise LDO (40 µVRMS) designed to absorb 400mA+ Wi-Fi RF transmission transients without voltage sag.
* **PCB Design:** Symmetrical 4-layer stackup (Signal - Ground Plane - Power Plane - Signal), 90Ω controlled differential impedance USB traces, Littelfuse AQ3045 TVS protection arrays, 0 DRC violations.
* 🔗 **[Explore Repository →](https://github.com/AakashdipDey/esp32-s3-usbc-devkit)**

---

### 2. [Smart Medication Dispensing & Biometric Telemetry System](https://github.com/AakashdipDey/smart-medibox-wearable-system)
*Synchronized dual-device IoT healthcare ecosystem comprising an automated base dispenser and a patient wearable.*
* **MediBox Base Station:**
  * **Gravimetric Pill Verification:** 7 independent medicine bays, each monitored by an **HX711 24-bit ADC / Load Cell Amplifier** with a synchronized master clock and 7 discrete serial data return lines.
  * **Automated Actuation:** 7 **SG90 micro servos** driven via dedicated hardware PWM channels for scheduled compartment dispensing.
  * **High-Current Power Stage:** **LM2596 switching buck converter** delivering up to 3A @ 5V with a 1000µF low-ESR bulk capacitor and 60mil power traces to withstand multi-servo stall currents.
  * **Reminders:** Addressable WS2812B RGB status strip and audible piezo buzzer.
* **Wearable Companion:**
  * **Form Factor:** Ultra-compact 4-layer wearable board powered by an **ESP32-S3-MINI** with onboard PCB antenna.
  * **Power Path Management:** Seamless automatic switching between USB-C and single-cell Li-Po battery using an ideal-diode P-Channel MOSFET (`DMG2305UX`) and Schottky diode (`MBR0520`).
  * **Battery Charging & Haptics:** **Microchip MCP73831** Li-Ion charger, discrete N-FET (`SI2302`) ERM vibration motor driver with flyback clamp diode, and 4-pin 0.5mm FPC sensor connector.
* 🔗 **[Explore Repository →](https://github.com/AakashdipDey/smart-medibox-wearable-system)**

---

### 3. [Precision Wireless Data Acquisition (DAQ) Card](https://github.com/AakashdipDey/esp32-s3-wireless-daq-card)
*Industrial-grade mixed-signal instrumentation card pairing microvolt-level analog conditioning with 240MHz wireless telemetry.*
* **Instrumentation Amplifier:** **Texas Instruments INA333** (25µV max offset, 0.5µV/°C drift, 100dB CMRR) for conditioning millivolt signals from strain gauges, RTDs, thermocouples, and current shunts.
* **16-Bit Digitization:** **Texas Instruments ADS1115** Delta-Sigma ADC featuring an integrated Programmable Gain Amplifier (ranges from ±256mV to ±6.144V) and internal low-drift reference.
* **Closed-Loop Control:** **Microchip MCP4725** 12-bit DAC with on-board EEPROM for baseline calibration, sensor excitation, and voltage bias offset injection.
* **Voltage Benchmark & Protection:** **Microchip LM4040** precision 2.5V shunt reference, **Littelfuse SMAJ26CA** 400W TVS surge diode, and AMS1117-3.3 power regulation.
* 🔗 **[Explore Repository →](https://github.com/AakashdipDey/esp32-s3-wireless-daq-card)**

---

## 📈 GitHub Overview

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=AakashdipDey&show_icons=true&theme=radical&hide_border=true&count_private=true" alt="Aakash's GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=AakashdipDey&layout=compact&theme=radical&hide_border=true" alt="Top Languages & Technologies" />
</div>

---

## 📬 Connect With Me

* **GitHub:** [@AakashdipDey](https://github.com/AakashdipDey)
* **Location:** Vellore, Tamil Nadu, India
* **Opportunities:** Open to Hardware Engineering, PCB Design, and Embedded Systems roles.

---
*Crafted with precision in Altium Designer.*
