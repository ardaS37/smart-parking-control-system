# Smart Parking Control System

<p align="center">
  <img src="3.png" alt="Yol Gösteren project logo" width="420" />
</p>

An Arduino-based smart parking prototype that identifies RFID cards and drives parking-entry responses through a display, indicator lights, audible alerts, and servo-controlled barriers.

> This repository documents a hardware prototype. It is intended for learning and demonstration purposes, not as a production access-control system.

## Recognition

**Teknofest 2021 — Smart Transportation Systems**

- Finalist project
- Ranked **6th** in the final scoring

This project was developed as an award-recognized smart transportation systems prototype for Teknofest 2021.

## Features

- RFID card identification with an RC522 reader
- Automated barrier control using two servo motors
- Status feedback through a 16×2 LCD, RGB LED, and buzzer
- Configurable responses for standard and alert categories
- Wiring diagram supplied as both an image and a Fritzing project
- Serial output for basic debugging during development

## Hardware

| Component | Purpose |
| --- | --- |
| Arduino Mega 2560 | Main controller |
| RC522 RFID reader | Card identification |
| 16×2 LCD | Status messages |
| 2 × servo motors | Barrier movement |
| RGB LED | Visual status indication |
| Buzzer | Audible alerts |
| HC-05 Bluetooth module | Shown in the wiring design for optional connectivity |

## Wiring Diagram

<p align="center">
  <img src="otopark_bb.jpg" alt="Smart Parking Control System wiring diagram" width="100%" />
</p>

The editable Fritzing design is available in [`otopark.fzz`](otopark.fzz).

## Getting Started

1. Open [`proje.ino`](proje.ino) in the Arduino IDE.
2. Install the required libraries:
   - `LiquidCrystal`
   - `Servo`
   - `SPI`
   - `RFID`
3. Assemble the hardware according to the wiring diagram.
4. Select **Arduino Mega 2560** as the board and upload the sketch.
5. Open the Serial Monitor at **9600 baud** to view card activity.

## RFID Demo Data

The RFID card identifiers currently included in [`proje.ino`](proje.ino) are **sample values used for demonstration purposes**. If you adapt this prototype for a real environment:

- Replace the sample values with your own locally managed configuration.
- Keep production card identifiers outside version control.
- Use a proper authentication and authorization design for real access control.

## Repository Structure

```text
.
├── proje.ino         # Arduino sketch
├── otopark.fzz       # Editable Fritzing design
├── otopark_bb.jpg    # Wiring diagram
└── 3.png             # Project logo
```

## License

This project is licensed under the [MIT License](LICENSE.md).

---

Built as a hardware and Arduino learning project by [ardaS37](https://github.com/ardaS37).
