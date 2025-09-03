# Wireless Digital Notice Board

The Wireless Digital Notice Board System is an embedded solution designed to provide a reliable, secure, and energy-efficient platform for digital communication. Built on the LPC2148 ARM7 microcontroller, the system wirelessly displays scrolling messages on a four-panel LED matrix. Messages are transmitted in real time from a smartphone via the HC-05 Bluetooth module, securely stored in AT24C256 EEPROM, and persist even after a power cycle.

This project is particularly suited for schools, offices, and public spaces where instant, authenticated, and continuous digital communication is required.

---

📋 **Project Overview**

The system integrates multiple hardware modules to create a robust wireless display solution:

- **Scrolling Message Display:** Text messages are displayed across a 4-panel (8×8) dot matrix LED display.
- **Wireless Updates:** Messages can be sent from a smartphone through Bluetooth.
- **Persistent Storage:** Messages are saved in EEPROM to ensure retention after power-off.
- **Secure Updates:** Only messages with a valid passkey (e.g., @153Your Message$) are accepted.
- **Continuous Scrolling:** Stored messages scroll automatically until updated.
- **Efficient Control:** Powered by the LPC2148 ARM7 microcontroller for speed and reliability.

---

🔧 **Hardware Components**

- LPC2148 (ARM7 Microcontroller)
- 4 × 8×8 Dot Matrix LED Displays
- HC-05 Bluetooth Module
- AT24C256 EEPROM (I2C-based)
- 74HC573 (Octal Latch)
- 74HC164 (Shift Register)

---

🗂 **Project Structure**
```
Major_Project/
├── delay.c / delay.h          # Delay functions
├── dml.c / dml.h              # Dot matrix LED control
├── i2c.c / i2c.h              # I2C protocol implementation
├── i2c_eeprom.c / .h          # EEPROM read/write
├── uart.c / uart.h            # UART communication
├── defines.h                  # Global definitions
├── projectmain.c              # Main source file
```

---

💡 **Features**

- Secure Bluetooth messaging with passkey authentication
- Scrolling of long messages across all LED matrices
- EEPROM-based message storage and retrieval
- Default message display when EEPROM is empty
- Continuous operation until new data is received

---

🛠 **Tools Used**

- Keil uVision (Embedded C development)
- Flash Magic (Programming LPC2148)
- Embedded C Language

---

🚀 **Getting Started**

1. Program LPC2148 using Flash Magic.
2. Pair a smartphone with the HC-05 module.
3. Send a message in the format: @153Hello World$.
4. The system validates, stores, and displays the message.

---

✅ **Status**

- Bluetooth communication – ✔
- EEPROM read/write – ✔
- Multi-panel dot matrix scrolling – ✔
- UART + I2C integration – ✔
- Passkey-based authentication – ✔

---

🌱 **Future Enhancements**

- LCD integration (16x2 / graphical displays)
- Dedicated Android mobile application
- Multi-language or symbolic message support
- Power-saving modes for extended operation
- EEPROM-based message history management

---

🙏 **Acknowledgments**

This project was developed as part of the Major Project at Vector India  
under the guidance of Mr. Chandramouli.

We express sincere gratitude to the faculty, mentors, and technical community whose resources and support enabled the successful completion of this work.

- Developed by: Syama Venkat Teja
- Institution: Vector India
- Guide: Mr. Chandramouli
- Project: Wireless Digital Notice Board using LPC2148
