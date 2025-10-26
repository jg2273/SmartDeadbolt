# Development Logbook

---

## Sept. 16, 2025

- Create and submit high-level block diagram
- Meeting after class about improvements
- Decided on LCD and LED outputs for user interface
- Scrapped the idea of traditional key modifications and FSR's (too complicated)

---

## Sept. 18, 2025

- Created GitHub Repository
- Finalized changes to repository and file structure

---

## Sept. 22, 2025

- Create and submit major component selection
  
---
## Sept. 23, 2025 

- Determining the type of microcontroller to use, due to the need of additional I/O pins from Arduino UNO R3
- Determining voltage regulation required to operate RFID
- Utiize AdaFruit to look into I2C configurations that will support RFID network

---
## Sept. 27, 2025

- Agreed on Arduino Mega as the microcontroller to prototype with, sufficient amount of I/O pins, doesn't require complex configuration
  
---


## Sept 30, 2025

- Created unit tests for various modules throughout the project schematic
- Created hierarchical sheets within Kicad for the schematic

---

## October 9, 2025

- Arduino Mega arrived in mail
- Unit test for Servo complete, controlled using push-button switches
- Unit test for LCD complete
- LCD programmed to display info when servo is activated
- Unit test for keypad complete, programmed with specific unlock code in Arduino IDE
- Keypad programmed to actiavte LCD output when input is detected, and replaced the push-button switches to activate servo

---

## October 11, 2025

- RFID troubleshooting (finding UID of our tags), resolved by opening wiring RFID and running serial monitor while scanning tag 
- RFID unit test complete
- RFID programmed to work as alternative to keypad, and also activate servo when scanned tag UID matches the UID in code

---
