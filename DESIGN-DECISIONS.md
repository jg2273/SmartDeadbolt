# Design Decisions

This document outlines the major design decisions made by out team during the development of the Smart Deadbolt Lock Project.

---

## Table of Contents
1. Overview
2. High Level Design
3. Hardware Design
4. Software Design
5. Enclosure

---

## 1. Overview
This project is a smart deadbolt lock that provides secure access control, and is built around an Arduino microcontroller to enable access via a keypad and RFID reader. Our team aimed to design a cost-effective, reliable and user-friendly locking mechanism suitable for residential use.

---

## 2. High Level Design

**Block Diagram**

![Block Diagram](./docs/block_diagram.jpeg)
**Decision:** Incorporating RFID 

**Reasoning:** Convenient and safe security measure for modular locking and unlocking system

**Decision:** Incorporating Keypad

**Reasoning:** Efficient alternative to RFID if user doesn't have proper RFID credentials

**Decision:** Incorporating GUI

**Reasoning:** Efficient method of interaction between user and modular system

---

## 3. Hardware Design

**Decision:** Using Arduino Mega microcrontoller

**Reasoning:** Provides sufficient amount of i/o pins, effective physical size for design

**Decision:** 3x4 Matrix Number Pad

**Reasoning:** Provides a robust design, less i/o pins required compared to others, numbers & 2 symbols only https://www.adafruit.com/product/3845


**Decision:** 

---

## 4. Software Design

**Decision:** Using Arduino IDE to program microcontroller

**Reasoning:** Simplest and most universal way to program microcontroller


---

## 5. Enclosure 

**Decision:**

**Reasoning:**



