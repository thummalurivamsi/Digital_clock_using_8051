⏰ Digital Clock using 8051 Microcontroller
This project demonstrates the implementation of a real-time digital clock using the AT89C51 microcontroller, designed to display the current time in HH:MM:SS format on a 16x2 LCD display. It uses Timer0 for precise time delay generation and updates the clock every second without any external RTC (Real-Time Clock) chip.

📌 Project Overview
Digital clocks are a fundamental embedded system project that helps in understanding how to use microcontroller timers and display modules. This project uses the internal Timer0 of the 8051 microcontroller to generate accurate time delays and updates the time variables (seconds, minutes, hours) accordingly. The current time is continuously displayed on a 16x2 LCD.

⚙️ Components Used
AT89C51 Microcontroller (8051)

16x2 LCD Display – For displaying the digital time

Power Supply Module – 5V regulated

Resistors & Capacitors – For reset and oscillator circuits

12MHz Crystal Oscillator

Push Buttons (optional for setting time)

Connecting Wires & Breadboard/PCB

🧠 Working Principle
The system uses Timer0 in mode 1 (16-bit) to generate a 10ms delay.

By looping this delay 100 times, a 1-second delay is achieved.

After every second:

Seconds (sec) are incremented.

Once seconds reach 60, they reset to 0 and increment minutes.

Similarly, once minutes reach 60, hours are incremented.

The hour counter resets after reaching 24.

The LCD is updated every second with the new time.

📟 LCD Display
The 16x2 LCD is used in 8-bit mode, with control lines connected to port P3.0 (RS) and P3.1 (EN). Data is sent via Port 2 (P2). The display is refreshed each second to show the current time.

Example display:
     14:23:08
💡 Features
Simple and effective timekeeping using software delays

Clear LCD display in HH:MM:SS format

Compact design suitable for microcontroller learning

Modular code with reusable functions

Easy to expand (e.g., add time-setting buttons or RTC integration)

📸 Project Media



📈 Future Improvements
Add time-setting buttons for hour/minute adjustments

Integrate DS1307 or DS3231 RTC for precise long-term accuracy

Add battery backup using a coin cell and RTC

Use interrupts instead of polling for better efficiency

Show date and day along with time

👨‍💻 Developed By
Vamsi T
Graduate Engineer (ECE)
📧 vamsithummaluri@gmail.com

🛠️ License
This project is licensed under the MIT License – feel free to use, modify, and share as needed.
