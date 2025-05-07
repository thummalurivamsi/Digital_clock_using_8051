# ⏰ Digital Clock using 8051 Microcontroller

This project demonstrates a real-time **digital clock** using the **AT89C51 microcontroller**, capable of displaying time in the **HH:MM:SS** format on a **16x2 LCD**. It uses **Timer0** to generate precise 1-second intervals for time updates—**no external RTC** module is required.

---

## 📌 Project Overview

Digital clocks are fundamental to embedded systems and provide hands-on experience in working with microcontroller **timers**, **delays**, and **LCD interfacing**. This project effectively illustrates the working of a simple software-based timekeeping system using the 8051's internal timer.

Every second, the microcontroller:

- Increments the seconds counter  
- Rolls over to minutes and hours appropriately  
- Refreshes the LCD to display updated time

---

## ⚙️ Components Used

- **AT89C51 Microcontroller (8051)**
- **16x2 LCD Display** – Shows time in `HH:MM:SS` format
- **12 MHz Crystal Oscillator** – For clock generation
- **Power Supply Module** – 5V regulated
- **Resistors & Capacitors** – For reset and oscillator circuit
- **Push Buttons** *(optional)* – For future time-setting enhancement
- **Breadboard or PCB**, **Connecting Wires**

---

## 🧠 Working Principle

- Timer0 is configured in **Mode 1 (16-bit)**.
- Timer is loaded to generate a **10 ms delay**.
- Looping this delay 100 times provides an accurate **1-second delay**.
- Time is updated and displayed:
  - When `sec == 60`, it resets to 0 and `min++`.
  - When `min == 60`, it resets to 0 and `hour++`.
  - When `hour == 24`, it resets to 0.

---

## 📟 LCD Display

The **16x2 LCD** operates in **8-bit mode**:

- **RS** = `P3.0`  
- **EN** = `P3.1`  
- **Data lines** = `Port 2 (P2)`

The display is cleared and refreshed every second to show the current time.

**Example Output:**
 14:23:08

---

## 💡 Features

- Real-time software clock using internal timer  
- LCD display in `HH:MM:SS` format  
- No need for external RTC  
- Clean, modular embedded C code  
- Ideal for students learning microcontroller-based development  
- Scalable for additional features  

---

## 📸 Project Media

![Digital_clock_8051_output](https://github.com/user-attachments/assets/78581fcd-deb8-475b-b145-586043403372)


---

## 📈 Future Improvements

- Add **push buttons** for manual time adjustment  
- Integrate **DS1307/DS3231 RTC** module for long-term accuracy  
- Add **battery backup** for time retention  
- Use **interrupt-based timing** instead of polling for efficiency  
- Display **date and day** along with time  
- Develop an **alarm function** with buzzer  

---

## 👨‍💻 Developed By

**Vamsi T**  
Graduate Engineer (ECE)  
📧 vamsithummaluri@gmail.com

---

## 🛠️ License

This project is licensed under the **MIT License** – feel free to **use**, **modify**, and **share** as needed.
