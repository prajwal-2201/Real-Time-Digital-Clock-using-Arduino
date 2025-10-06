# 🕒 Real-Time Digital Clock using Arduino

A **real-time digital clock system** built with **Arduino UNO** that displays the **time, date, day, and temperature** on an LCD screen.  
It combines **sensors**, **servo motion**, and **smart power-saving features** to create an interactive and intelligent clock.

---

## 🧩 Features

- ⏰ **Real-time display** of hours, minutes, seconds, date, and day  
- 🌡️ **Temperature monitoring** using the DHT11 sensor  
- 🧠 **Accurate timekeeping** with the RTC (Real-Time Clock) module  
- ✋ **Motion-activated display** — LCD turns ON when a hand is near (using ultrasonic sensor)  
- ⚙️ **Servo motor indicator** — rotates to show system activity  
- 🔋 **Power-efficient** — display sleeps automatically when no motion is detected  

---

## 🛠️ Hardware Components

| Component | Description |
|------------|-------------|
| **Arduino UNO** | Main microcontroller board |
| **RTC Module (DS3231/DS1307)** | Keeps accurate time even when powered off |
| **DHT11 Sensor** | Measures ambient temperature |
| **Ultrasonic Sensor (HC-SR04)** | Detects proximity of a hand |
| **16x2 LCD Display** | Shows time, date, day, and temperature |
| **Servo Motor** | Provides visual feedback (pointer movement) |
| **Jumper Wires & Breadboard** | Circuit connections |

---

## ⚡ Circuit Overview

The system integrates sensors and modules as shown in the block diagram:

```
[Ultrasonic Sensor] ─┐
                     │
[DHT11 Sensor] ─────> Arduino UNO ─────> [LCD Display]
                     │
[RTC Module] ────────┘
                     ↓
               [Servo Motor]
```

- The **RTC module** provides current time data.
- The **DHT11 sensor** sends temperature readings.
- The **Ultrasonic sensor** detects motion to control the LCD and servo motor.

---

## 🧠 Working Principle

1. **Initialization:** Arduino reads real-time data from the RTC and DHT11 sensors.  
2. **Display Logic:**  
   - If a hand is detected near the sensor, the LCD display turns ON.  
   - When no movement is detected, the display automatically turns OFF.  
3. **Servo Action:** The servo motor pointer moves when the clock is active.  
4. **Continuous Update:** The clock refreshes time and temperature readings every second.

---

## 🧾 Code

The complete source code is available in [`mpca_the_goat.ino`](./mpca_the_goat.ino).  
You can upload it directly to your **Arduino UNO** using the **Arduino IDE**.

---

## 🧰 Libraries Used

Make sure the following libraries are installed in your Arduino IDE:

- `Wire.h`
- `RTClib.h`
- `LiquidCrystal.h`
- `Servo.h`
- `DHT.h`

To install:
```
Sketch → Include Library → Manage Libraries → Search and Install
```

---

## 📸 Project Team

| Name | Student ID | Role |
|------|-------------|------|
| **Poorva Reddy** | PES2UG23CS416 | Hardware & Testing |
| **Sipivishta** | PES2UG23CS412 | Coding & Integration |
| **Prajwal** | PES2UG23CS424 | Circuit Design |
| **Swetha Patil** | — | Faculty Guide |

---

## 🧑‍💻 Setup Instructions

1. **Connect all components** as per the circuit diagram.  
2. **Open the code** in Arduino IDE.  
3. **Select the correct board and COM port** under Tools → Board → *Arduino UNO*.  
4. **Upload the code**.  
5. Observe the display and sensor responses in real time.

---

## 📷 Demo & Poster

You can view the complete project poster and explanation here:  
[`REAL_TIME_DIGITAL_CLOCK_POSTER.pdf`](./REAL_TIME_DIGITAL_CLOCK_POSTER.pptx%20(4).pdf)

---

## 🧾 License

This project is open-source and free to use for educational purposes.  
Feel free to modify or improve it with proper credit.

---

### 💡 “A simple clock made smart — blending sensors, motion, and design.”



