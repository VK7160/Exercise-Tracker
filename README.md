# Exercise-Tracker

> C++ · Arduino · Raspberry Pi · ESP8266 · Vansh Khanna

A hardware-software exercise tracking system that uses **biometric attendance** (fingerprint sensor), **motion sensing** (accelerometer), **environmental monitoring** (temperature & humidity), and an **OLED display** — all coordinated via a Raspberry Pi and ESP8266 microcontrollers.

---

## Problem Statement

Built to explore embedded systems and IoT integration: how do you track physical activity and attendance reliably using low-cost hardware? This project combines multiple sensors into a unified data collection system.

---

## Features

- **Fingerprint-based attendance** — identifies and logs users via ESP8266 + OLED display (`Fingerprint_Oled_Esp8266.ino`)
- **Accelerometer motion tracking** — detects movement/exercise activity (`SimpleAccelerometer.ino`)
- **Temperature & Humidity monitoring** — logs environmental conditions during workouts (`Temp_Hum.ino`)
- **Raspberry Pi coordination** — central data aggregation script in Python (`Raspberrypi.py`)
- **Web dashboard** — basic HTML front-end for viewing exercise logs (`Exercise.html`)
- **Biometric attendance archive** — stored records (`biometricattendance.rar`)

---

## Hardware List

| Component | Purpose |
|---|---|
| Raspberry Pi | Central controller & data logger |
| ESP8266 (NodeMCU) | Wi-Fi microcontroller for fingerprint/OLED |
| Fingerprint Sensor | User identification & attendance |
| OLED Display | Real-time feedback on device |
| Accelerometer | Motion/exercise detection |
| DHT Sensor | Temperature & humidity readings |

---

## Build & Run

**Arduino sketches** (upload via Arduino IDE):
```
Fingerprint_Oled_Esp8266.ino  → Upload to ESP8266
SimpleAccelerometer.ino       → Upload to Arduino board
Temp_Hum.ino                  → Upload to Arduino board
```

**Raspberry Pi script**:
```bash
python3 Raspberrypi.py
```

**Web dashboard** — open `Exercise.html` in any browser.

---

## What I'd Improve Next

- Replace the HTML front-end with a lightweight Flask or Node.js API
- Store sensor data in a local SQLite or InfluxDB database
- Add real-time Grafana dashboard for workout visualisation
- Improve fingerprint enrolment UX with a guided serial prompt

---

*Vansh Khanna — VK7160*
