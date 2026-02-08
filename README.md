# Arduino Weather Monitor (DHT11 + LCD)

## 📌 Project Overview
This project is an autonomous environmental monitoring station designed to measure ambient temperature and humidity. It provides real-time data visualization on an LCD screen and tracks extreme climate values (Minimum and Maximum) during the session.

The main goal of this project was to create a reliable, jitter-free monitoring system using optimized C++ code for embedded systems.

## 🛠 Features
* **Real-time Monitoring:** Continuous data acquisition from the DHT11 sensor.
* **Data Logging:** Tracks and displays Min/Max temperature and humidity levels.
* **Optimized UI:** Implemented non-blocking timing logic to prevent LCD flickering and ensure smooth data updates.
* **Autonomous Operation:** Designed to run 24/7 without manual intervention.

## 🧱 Hardware Components
* **Microcontroller:** Arduino Uno (or compatible)
* **Sensor:** DHT11 (Temperature & Humidity)
* **Display:** LCD 16x2 (via I2C or Parallel interface)
* **Others:** Resistors, Potentiometer (for contrast), Breadboard, and Jumper wires.

## 💻 Software & Libraries
* **Language:** C++ (Arduino Sketch)
* **Libraries used:** * `DHT.h` (Adafruit)
  * `LiquidCrystal.h` (or `LiquidCrystal_I2C.h`)

## 🚀 How to Use
1. Clone this repository.
2. Connect the hardware according to the circuit diagram (see `/images` folder).
3. Open the `.ino` file in Arduino IDE.
4. Upload the code to your board.
