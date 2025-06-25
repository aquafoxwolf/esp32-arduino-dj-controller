# **DIY Arduino and ESP32 based DJ Controller**

This is custom-built DJ controller project based on combination of ESP32 and Arduino boards. It uses multiple potentiometers and buttons as well as it uses build it display of CYD - esp32 based board to display waveforms and current tracks info.

## **Overview**
Controller is combined of multiple microcontrollers:
- ESP32-C3 SuperMini - Handles remote comminication between users PC and CYD for sending waveform and songs data
- CYD (Cheap Yellow Display model: ESP32-2432S028 aka cyd2usb) - Handles displaying waveform and song information like BPM, time, track name