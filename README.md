# Pico-Security-System
This repository contains a multi-sensor security and access control system built using the Raspberry Pi Pico. The project integrates laser-based intrusion detection, flame hazard monitoring (Fire detection), and RFID-based access control to create a versatile, real-time security solution.

# Features
1. Intrusion Detection
   Uses a laser and photoresistor (LDR) to monitor for interruptions.
   Triggers alerts with flashing LEDs, buzzer sounds, and a warning message on an I2C LCD display.
2. Flame Detection:
   Continuously monitors for fire hazards using a flame sensor (ky 026).
   Displays "Fire Alert" message and activates alarms for evacuation.
3. RFID Access Control:
   Reads RFID cards to grant or deny access
   Authorized cards display "Access Granted, " activate green LED, and turn off laser       
   momentarily. Unauthorized card trigger 
   "Access Denied" warnings with buzzer alerts. 
4. Real-Time Alerts:
   Combines RGB LEDs, buzzer, and an LCD screen for visual, audio, and textual notifications.

# Componets Used
1. Raspberry Pi Pico
2. MFRC522 RFID Module
3. I2C LCD 16by2 Display
4. Laser Module (ky008)
5. photoresistor (LDR)
6. Flame Sensor (ky026)
7. RGB LED
8. Buzzer

# How it works

1. Intrusion Detection: The laser shines on an LDR. If the beam is interrupted, the system triggers an intruder alert.
2. Flame Detection: A flame sensor detects fire, prompting evacuation alerts and alarms.
3. RFID Control: The RFID module reads card IDs. If a valid card is detected, access is granted; otherwise, access is denied, and an alert is raised.

# Setup
1. Connect all components as per the wiring instructions in the documentation.
2. Install the required libraries:
   pico_i2c_lcd for the I2C LCD
   MFRC522 library for RFID module support
3. Flash the provided code onto your Raspberry Pi Pico

Contributions are welcome! Feel free to fork the repository, submit issues, or add enhancements to improve the system
