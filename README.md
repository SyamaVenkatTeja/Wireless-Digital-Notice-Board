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
