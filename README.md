# 📡 Smart IoT-Based Antenna Position and Monitoring System

An intelligent IoT-based antenna positioning system that automatically aligns a directional antenna to the position with the strongest Wi-Fi signal using RSSI (Received Signal Strength Indicator). The system supports both **Manual** and **Automatic** operation through the Blynk IoT platform while displaying real-time information on a 16×2 LCD.

---

## 📖 Overview

Proper antenna alignment is essential for achieving strong and stable wireless communication. Manual antenna positioning is time-consuming and often inaccurate, especially in remote or changing environments.

This project uses an **ESP32** to monitor Wi-Fi signal strength (RSSI) and control two servo motors that rotate the antenna along the **X-axis** and **Y-axis**. In automatic mode, the ESP32 scans multiple positions, identifies the strongest signal, and aligns the antenna accordingly. In manual mode, users can control the antenna remotely using the **Blynk IoT** mobile application.

The system also monitors **temperature** and **humidity** using a **DHT11 sensor** and displays all important information on an LCD and the Blynk dashboard.

---

# ✨ Features

- 📡 Automatic antenna alignment using Wi-Fi RSSI
- 🎮 Manual antenna control using the Blynk mobile app
- 📶 Real-time RSSI monitoring
- 🌡 Temperature monitoring using DHT11
- 💧 Humidity monitoring using DHT11
- 📱 IoT monitoring with Blynk Cloud
- 📟 16×2 LCD real-time display
- ⚙ Dual-axis antenna movement (X & Y)
- 🔋 Battery-powered portable system
- ☁ Wi-Fi connectivity using ESP32

---

# 🛠 Hardware Used

| Component | Quantity |
|-----------|---------:|
| ESP32 Development Board | 1 |
| 180° Servo Motor | 2 |
| DHT11 Temperature & Humidity Sensor | 1 |
| 16×2 LCD Display | 1 |
| I2C LCD Module | 1 |
| 18650 Li-ion Battery | 2 |
| 2S Battery Management System (BMS) | 1 |
| Buck Converter (7.4V → 5V) | 1 |
| ON/OFF Switch | 1 |
| PVC Frame & Servo Brackets | 1 Set |
| Directional Antenna | 1 |

---

# 💻 Software Used

- Arduino IDE
- ESP32 Board Package
- Blynk IoT
- ESP32Servo Library
- LiquidCrystal_I2C Library
- DHT Sensor Library

---

# ⚙ Working Principle

## Manual Mode

- The user controls the X-axis and Y-axis using sliders in the Blynk application.
- Servo motors move according to the selected angles.
- LCD continuously displays:
  - X Position
  - Y Position
  - Temperature
  - Humidity
  - RSSI
  - Current Mode

---

## Automatic Mode

When Auto Mode is enabled:

1. ESP32 rotates both servos through predefined angles.
2. Wi-Fi RSSI is measured at every position.
3. The strongest RSSI value is stored.
4. After scanning is complete, the antenna automatically moves to the best position.
5. The antenna remains at the optimal angle until another scan is started.

---

# 📟 LCD Display

### Manual Mode

```
X:180 Y:120 T:30
RSSI:-45 H:65 M
```

### Auto Scanning

```
X:120 Y:60 T:30
RSSI:-52 H:64 S
```

### Auto Mode (Best Position)

```
X:150 Y:90 T:30
RSSI:-38 H:63 A
```

Where:

- **M** = Manual Mode
- **S** = Scanning
- **A** = Auto Mode (Best Position Locked)

---

# 📱 Blynk Dashboard

| Virtual Pin | Function |
|-------------|----------|
| V0 | X-Axis Slider |
| V1 | Y-Axis Slider |
| V2 | Auto / Manual Switch |
| V3 | RSSI SuperChart |
| V4 | Temperature Display |
| V5 | Humidity Display |
| V7 | X Position Display |
| V8 | Y Position Display |

---

# 🔌 ESP32 Pin Connections

| Component | ESP32 Pin |
|-----------|-----------|
| X Servo | GPIO18 |
| Y Servo | GPIO19 |
| DHT11 | GPIO4 |
| LCD SDA | GPIO21 |
| LCD SCL | GPIO22 |

---

# 📂 Project Structure

```
Smart-IoT-Antenna-Positioning-System/
│
├── code/
│   └── Smart_Antenna.ino
│
├── images/
│   ├── prototype.jpg
│   ├── lcd.jpg
│   ├── blynk_dashboard.jpg
│   ├── wiring_diagram.png
│   └── block_diagram.png
│
├── circuit/
│   ├── Circuit_Diagram.pdf
│
├── docs/
│   ├── Project_Report.pdf
│
└── README.md
```

---

# 📸 Project Images

![alt text](<picture/WhatsApp Image 2026-05-12 at 5.28.38 AM.jpeg>)
---

## Hardware Prototype

![alt text](<picture/WhatsApp Image 2026-05-12 at 5.28.39 AM.jpeg width="50%" >)

---

## LCD Output

![alt text](<picture/IMG202605120517581.jpg width="50%" >)
---

## Blynk Dashboard

![alt text](<picture/Screenshot 2026-05-12 051508.png width="50%" >)
---

## Circuit Diagram

![alt text](<picture/Screenshot 2026-02-27 102001.png width="50%" >)

---

# 🚀 Future Improvements

- Continuous background RSSI optimization
- OTA firmware updates
- OLED/TFT graphical display
- MQTT support
- Data logging to cloud
- Battery voltage monitoring
- GPS-assisted antenna positioning
- Automatic periodic rescanning
- Web dashboard for monitoring

---

# 👨‍💻 Author

**Sandeep Koviri**

Master of science ( Computer science)Student

Passionate about:

- Internet of Things (IoT)
- Embedded Systems
- ESP32 Development
- Wireless Communication
- Automation
- AI-based Smart Systems

---

# ⭐ If you found this project useful

If you like this project, consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates future improvements.

---
