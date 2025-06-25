# WIP not finished
# **DIY Arduino and ESP32 based DJ Controller**

This is custom-built DJ controller project based on combination of ESP32 and Arduino boards. It uses multiple potentiometers and buttons as well as it uses build it display of CYD - esp32 based board to display waveforms and current tracks info.

## **Overview**
### 🧠 Controller is combined of multiple microcontrollers:
- ESP32-C3 SuperMini - Handles remote comminication between users PC and CYD for sending waveform and songs data
- CYD (Cheap Yellow Display model: ESP32-2432S028 aka cyd2usb) - Handles displaying waveform and song information like BPM, time, track name
- Arduino Mega - Handles most of the inputs
- Arduino Leonardo - Handles few potentiometers and MIDI output

### 🎛️ Hardware Componens:
- 1x ESP32-C3 SuperMini
- 1x CYD ESP32 based board
- 1x Arduino Mega
- 16x 10kOhm Potentiometers
- 5x 10kOhm Slider Potentiometers
- ?x Push Buttons (not yet counted)

### ⚙️ Features
- Real time display of tracks parameters and waveforms on CYD display
- Inputs connected to Arduino Mega get sent via serial to Arduino Leonardo and send out as MIDI output to pc
- Info about tracks gets send to ESP32-C3 SuperMini via usb and then get sent wirelessly via ESP-NOW to CYD
- Made to work with any DJ software that supports MIDI inputs (currently only testes with Mixxx)

### ⚡Wiring (schematics to be added later)
- Arduino Mega reads analog/digital inputs and sends data over serial to Leonardo
- Arduino Leonardo receives serial data and reads its own additional analog inputs and outputs MIDI over usb
- ESP32-C3 receives data and sends it via ESP-NOW to CYD
- CYD receives info wirelessly (only connected to power)

### 💿 Software
**Required Programs**:
- Arduino IDE
- Python3

**ArduinoIDE Libraries**:
- esp_now
- TFT_eSPI
- WiFi
- MIDIUSB

**Python Libraries**:
- serial
- time
- pillow
- numpy
- pytesseract