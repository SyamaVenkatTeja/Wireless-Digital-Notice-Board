# Wireless Digital Notice Board

## Project Overview

This project implements a smart, interactive wireless display system that integrates several hardware modules for seamless digital communication. The system is ideal for campuses, offices, and public spaces.

### Features

- **🖥️ Scrolling LED Display**:  
  Displays messages as scrolling text across a 4-panel 8×8 dot matrix LED display.

- **📱 Bluetooth Connectivity**:  
  Receives messages wirelessly from a smartphone via the HC-05 Bluetooth module.

- **💾 EEPROM Storage**:  
  Saves incoming messages to an AT24C256 EEPROM, ensuring persistence even after power cycles.

- **🔐 Secure Message Update**:  
  Only updates displayed messages when the incoming message contains a valid passkey (`@153Your Message$`).

- **🔁 Auto-Scrolling**:  
  Continuously scrolls the stored message until a new message is received.

- **🧠 Fast MCU Control**:  
  Built on the ARM7-based LPC2148 microcontroller for reliable, high-speed operation.

- **🔀 SIPO Shift Register**:  
  Uses a serial-in, parallel-out (SIPO) shift register (handled by `sipo.c`) for driving the LED matrix display.

---

## Hardware Components

- **LPC2148** (ARM7 Microcontroller)
- **4 × 8×8 Dot Matrix LED Displays**
- **HC-05 Bluetooth Module**
- **AT24C256 EEPROM** (I2C-based)
- **74HC573** (Octal Latch)
- **74HC164** (Shift Register)

---

This system is easy to use, secure, and perfect for enhancing digital communication in public spaces. 🚀

---

## 💡 Features

- Send text messages via Bluetooth using a passkey (e.g., @153Message$)
- Scroll long messages across all 4 LED matrices
- Store and retrieve messages using EEPROM (AT24C256)
- Continuously display stored messages until a new one is received
- Default message shown if EEPROM is empty
- Efficient LED control using SIPO logic

---

## 🛠 Tools Used
- Keil uVision (Embedded C development)
- Flash Magic (Programming LPC2148)
- Embedded C Language

---

## 🚀 How to Use

### 1. Build the Firmware
- Open the source code in Keil uVision.
- Ensure all required files are present:
    - projectmain.c (main logic)
    - delay.c, dml.c, i2c.c, i2c_eeprom.c, uart_init.c, sipo.c and their respective headers
    - defines.h, types.h (global definitions)
- Compile the project to generate the HEX file for LPC2148.

### 2. Flash the Microcontroller
- Use Flash Magic to program the compiled HEX file onto the LPC2148 microcontroller.
- Confirm successful flashing before proceeding.

### 3. Set Up the Hardware
- Connect the LPC2148 board to:
    - 4 × 8×8 Dot Matrix LED displays (via latch and shift register)
    - HC-05 Bluetooth module (for wireless communication)
    - AT24C256 EEPROM (for message storage)
- Power on the board and ensure all modules are functioning.

### 4. Bluetooth Pairing & Messaging
- On your smartphone, enable Bluetooth and pair with the HC-05 module.
- Install a serial/Bluetooth terminal app (e.g., Serial Bluetooth Terminal).
- Send messages in the format:  
  `@153Your Message$`  
  Replace Your Message with your desired text.
- Only messages with the correct passkey (@153...$) will be accepted and stored.

### 5. View & Update Display
- The current message will scroll across all 4 LED panels.
- The last valid message is stored in EEPROM and will persist after power cycles.
- To update the display, simply send a new message with the same passkey format.

### 6. Troubleshooting
- If the display doesn’t update, verify hardware connections and power.
- Ensure your message contains the correct passkey and format.
- Check EEPROM, Bluetooth, and SIPO connections.

---

## ✅ Status
- Bluetooth communication ✔️
- EEPROM read/write ✔️
- 4-panel dot matrix scrolling ✔️
- UART + I2C integration ✔️
- SIPO-based LED driving ✔️
- Passkey-based security ✔️

---

## 💡 Hardware Highlights
- **ARM7 Development Board Integration 🔗**: Centralized processing with LPC2148 microcontroller.
- **I2C Communication Protocol 🔄**: Efficient interfacing with peripheral devices using I2C for reliable data exchange.
- **UART Interrupt-driven Messaging 🚦**: Real-time wireless data transmission with UART interrupts for responsive communication.
- **Dynamic LED Matrix Display 🟩**: Multi-panel dot matrix modules for clear, vibrant message visualization.
- **Interactive LCD Interface 🖥️**: Character LCD for status updates and user feedback.
- **User-friendly Controls ⌨️**: Push buttons and 4x4 keypad for intuitive user interaction.
- **Sensor Connectivity 🌡️**: On-board ADC for analog sensor integration.
- **Modular Wiring 🧩**: Organized and scalable hardware connections for easy maintenance and upgrades.
- **SIPO-based Output Control 🧠**: sipo.c logic enables precise control of LEDs using fewer microcontroller pins.

---

## 🔧 Improvements & Future Enhancements
- **LCD Integration 📟**: While this project uses 8×8 dot matrix displays, it can be extended to work with an LCD (like 16x2 or graphical LCDs) for clearer, more flexible message display.
- **Mobile App Interface 📱**: Create a simple Android app to send and manage messages easily over Bluetooth.
- **Multi-Language Support 🌐**: Enhance character encoding to support local languages or symbols.
- **Power Efficiency 💡**: Use LPC2148’s low-power modes to reduce energy consumption in idle states.
- **Message Management 🗂️**: Implement EEPROM history to view or restore previously displayed messages.
- **Dynamic Matrix Expansion ➕**: SIPO logic (sipo.c) can be scaled for additional LED panels.

---

## 🤝 Contributing
Developed as part of Embedded Systems Training  
Based on ARM7 LPC2148 architecture  
Guided by trainers from Vector India

---

## 🙏 Acknowledgments
- 🎓 Developed by: Venkata Teja
- 🏫 Major Project
- 🎯 Tech: LPC2148, Embedded C, 8*8 LED Matrix, HC-05(Bluetooth), AT24C256(EEPROM).
