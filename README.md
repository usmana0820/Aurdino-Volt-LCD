# ⚡ Arduino ZMPT101B Voltage Sensor with LCD Display

An Arduino-based voltage monitoring project that uses the **ZMPT101B sensor** and a **16×2 I2C LCD** to display voltage readings in real time.

> **Note:** Confirm AC/DC measurement capabilities against your actual Arduino sketch and circuit before claiming both.

## ✨ Features

- Real-time voltage monitoring
- ZMPT101B sensor integration
- 16×2 LCD display with I2C
- Serial Monitor output for debugging
- Adjustable sensor sensitivity for calibration

## 🧰 Components Required

| Component | Purpose |
|---|---|
| Arduino Uno or compatible board | Main controller |
| ZMPT101B voltage sensor module | AC voltage measurement |
| 16×2 LCD with I2C interface | Displays readings |
| Jumper wires | Circuit connections |
| USB cable | Programming and serial monitoring |

## 📚 Libraries Required

Install these libraries through the Arduino IDE Library Manager, or use the linked repositories.

- [ZMPT101B Library](https://github.com/rrobinet/ZMPT101B)
- [LiquidCrystal_I2C Library](https://github.com/fdebrabander/Arduino-LiquidCrystal-I2C-library)

## 🔌 Circuit Diagram

Add your actual circuit diagram to the repository at:

`images/circuit-diagram.png`

Then display it in this section:

![Arduino ZMPT101B voltage sensor circuit diagram](images/circuit-diagram.png)

**Suggested connections** — verify these against your specific modules and sketch:

| Component | Arduino connection |
|---|---|
| ZMPT101B OUT | A0 |
| ZMPT101B VCC | Compatible supply voltage |
| ZMPT101B GND | GND |
| I2C LCD SDA | A4 on Arduino Uno |
| I2C LCD SCL | A5 on Arduino Uno |
| I2C LCD VCC/GND | Compatible supply and GND |

*The image will display once `images/circuit-diagram.png` has been added to the repository.*

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/usmana0820/Aurdino-Volt-LCD.git
cd Aurdino-Volt-LCD
```

### 2. Install the libraries

Open Arduino IDE and install the ZMPT101B and LiquidCrystal_I2C libraries.

### 3. Connect the components

Wire the sensor output to A0 and connect the I2C LCD to the appropriate SDA and SCL pins for your Arduino board.

### 4. Configure sensitivity

If your sketch defines a `SENSITIVITY` constant, adjust it using a safe calibration procedure and compare readings with a suitable reference meter.

### 5. Upload the sketch

Open `voltage_sensor_lcd.ino`, select your Arduino board and port, and upload the code.

### 6. View the readings

Open the Serial Monitor at the baud rate specified in your sketch. The LCD should display the measurements supported by your implementation.

## 💻 Code Overview

- **`setup()`** — Initializes serial communication, the sensor configuration, and the LCD.
- **`loop()`** — Repeatedly reads measurements and updates the serial output and display.

The exact behavior depends on the implementation in `voltage_sensor_lcd.ino`.

## ⚠️ Safety and Calibration

- The ZMPT101B is designed for AC voltage sensing; do not assume it can measure DC voltage.
- Verify the module's voltage rating and wiring before use.
- AC mains voltage can cause fatal electric shock. Do not handle exposed live wiring, and use appropriate isolation and enclosure precautions.
- Calibrate the sensor against a suitable reference instrument before relying on its readings.
- Never connect AC mains directly to an Arduino input.

## 👩‍💻 Author

**Usmana Zulfiqar**

- **Email:** [usmanazulfiqar20@gmail.com](mailto:usmanazulfiqar20@gmail.com)
- **GitHub:** [usmana0820](https://github.com/usmana0820)

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details, if included in the repository.

---

If you find this project useful, consider giving the repository a ⭐ on GitHub.
