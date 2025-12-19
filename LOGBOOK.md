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
## October 10, 2025

- Locking mechanism designed and 3D printed

---

## October 11, 2025

- RFID troubleshooting (finding UID of our tags), resolved by opening wiring RFID and running serial monitor while scanning tag 
- RFID unit test complete
- RFID programmed to work as alternative to keypad, and also activate servo when scanned tag UID matches the UID in code

---

## October 9, 2025

- 9V battery setup does not supply sufficient current to operate the entire design
- While operating on 9V battery, when servo activates, it draws too much current which makes other components have unexpected behavior
- Researching other possible power sources that fit project definition constraints
  
---
## October 14, 2025

- RFID troubleshooting, specific pins were programmed to have specific functions, RFID was not wired to those pins, and did not work, resolved

---

## December 1, 2025

- Began PCB design: implementing bare ATmega2560, programmer, voltage regulation, buzzer, RGB LED, headers for servo, RFID, keypad, LCD
- Using 4 AA batteries due to proper headspace for running ATmega and other components at 5V after regulation
- Implemented buck-boost converter for high efficiency in stepping down 6-6.5V to 5V

---

## December 4, 2025

- Implemented linear regulator (LDO) from 5V regulation to power RFID, since it runs at 3.3V, used linear regulator and not another due to RFID noise sensitivity, and low-noise output from linear regulation
- Used level switcher to convert 5V communiation ouputs from ATmega to 3.3V for RFID

---

## December 6, 2025

- Designed enclosure for prototype through wood-cutting
- Implemented level-switcher onto physical prototype

---

## December 7, 2025

- In PCB design, used bottom layer as ground plane, as well as ran vias from top to bottom for decoupling capacitors

---

## December 18, 2025

- Project report developed, project complete

--- 

# Major Takeaways

- Arduino Uno can be configured to have additional pins using i/o expanders, which use I2C (SDA, SCL). However, we opted to use the Arduino Mega, which uses the ATmega2560, and comes with 50 total more i/o pins
- Unit testing: this is the most efficient and optimized way to conduct rapid prototyping. Using unit testing, we finished the majority of our project within the span of a week
- RFID troubleshooting skills: Programming the receiver to respond to specific UID provided
- A 9V battery is not optimal for high current in embedded design. With a capacity  of 400-600 mAh at low current, the entire system browns out with high load like servo active in short spans. Due to the high demand, it pulls voltage supply down which browns out the Arduino and other components. For applications similar to ours, 4x AA battery supply is optimal, due to its ability to deliver current better as a result of a lower internal resistance in the batteries.
- Buck-boost converters paired with LDO linear regulators is a reliable power distribution network within most applications, and buck converters are much more efficient than LDOs.

