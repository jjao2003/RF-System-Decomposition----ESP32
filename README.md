# 📡 RF System Decomposition – ESP32
Wireless and Radiotechnology Course 2026

---

## 👤 Student Information
Name: Agozie Onuigbo  
Student ID: [Insert Your Student ID]

---

## 📌 Selected Device
Device: ESP32 (Wi-Fi + Bluetooth SoC)  
Manufacturer: Espressif Systems  
Datasheet Link:  
https://www.espressif.com/sites/default/files/documentation/esp32_datasheet_en.pdf

---

# 🔎 1. Introduction

This project analyzes the RF system architecture of the ESP32 System-on-Chip (SoC).  
The goal is to understand how digital data flows through RF blocks during transmission and reception.

The ESP32 integrates:
- Dual-core MCU
- Wi-Fi transceiver
- Bluetooth transceiver
- Power Amplifier (PA)
- Low Noise Amplifier (LNA)
- RF Matching Network
- Antenna interface

---

# 🧩 2. Simplified RF System Block Diagram

## 📤 Transmission Path

MCU/Baseband  
→ Modulator  
→ RF Transmitter  
→ Power Amplifier (PA)  
→ RF Matching Network  
→ Antenna  

---

## 📥 Reception Path

Antenna  
→ RF Matching Network  
→ Low Noise Amplifier (LNA)  
→ RF Receiver  
→ Demodulator  
→ MCU/Baseband  

---

# 📡 3. RF Block Explanations

## 1️⃣ MCU / Baseband Processor
The MCU generates and processes digital communication data.  
It runs WiFi and Bluetooth protocol stacks and prepares digital signals for transmission.

---

## 2️⃣ Modulator
The modulator converts digital bits into RF waveforms.  
WiFi uses OFDM modulation, while Bluetooth uses GFSK modulation.

---

## 3️⃣ RF Transmitter
The RF transmitter upconverts the baseband signal to the 2.4 GHz ISM band carrier frequency.

---

## 4️⃣ Power Amplifier (PA)
The PA increases the power of the RF signal before it is transmitted through the antenna, enabling longer communication range.

---

## 5️⃣ RF Matching Network
This block matches impedance (typically 50 Ω) between RF circuitry and antenna.  
It also filters harmonics and unwanted frequencies.

---

## 6️⃣ Antenna Interface
The antenna converts electrical RF signals into electromagnetic waves during transmission.  
During reception, it converts electromagnetic waves into electrical signals.

---

## 7️⃣ Low Noise Amplifier (LNA)
The LNA amplifies very weak received signals while adding minimal noise, improving receiver sensitivity.

---

## 8️⃣ RF Receiver
The RF receiver downconverts the incoming RF signal to baseband frequency for processing.

---

## 9️⃣ Demodulator
The demodulator extracts digital data from the received RF waveform.

---

# 🔄 4. Signal Flow Summary

### Transmission:
Application Data  
→ MCU  
→ Modulation  
→ RF TX  
→ PA  
→ Matching Network  
→ Antenna  
→ Air  

### Reception:
Air  
→ Antenna  
→ Matching Network  
→ LNA  
→ RF RX  
→ Demodulation  
→ MCU  

---

# 📂 Repository Structure

ESP32_RF_System_Decomposition/
│
├── README.md
├── rf_block_diagram.png
└── ESP32_RF_System_Decomposition_Report.pdf

---

# 🎯 Conclusion

The ESP32 integrates digital processing and RF hardware into a single chip.  
Understanding these RF blocks provides essential system-level knowledge required for IoT, embedded systems, and wireless engineering careers.
