# Mini Tank Robot 🤖🚜

A two-drive tracked robot I built using an Arduino-compatible platform. No welding involved, just solid, beginner-friendly hardware powered by two 18650 batteries, with infrared remote control and an 8x16 LED display for visual feedback.

## Features

- **Infrared remote control:** drive the tank forward, backward, left, and right using an IR remote
- **Servo-mounted "head":** the tank can look left and right on command
- **8x16 LED matrix display:** shows animations and status indicators for each movement (forward, back, left, right, stop)
- **Personalised nameplate:** pressing a dedicated button on the IR remote displays my name ("ADON") on the LED panel
- **Dual-motor tank drive:** independent PWM control of left and right motors for precise movement

## Hardware

| Component | Pin |
|-----------|-----|
| Left motor direction | D13 |
| Left motor PWM | D11 |
| Right motor direction | D12 |
| Right motor PWM | D3 |
| Servo | D9 |
| IR receiver | A0 |
| LED matrix SDA | A4 |
| LED matrix SCL | A5 |

**You'll also need:** 2x 18650 batteries (not included in most kits).

## Remote Control Mapping

| Button (Hex) | Action |
|--------------|--------|
| `0xFF629D` | Move forward |
| `0xFFA857` | Move backward |
| `0xFF22DD` | Turn left |
| `0xFFC23D` | Turn right |
| `0xFF02FD` | Stop |
| `0xFF30CF` | Rotate anticlockwise |
| `0xFF7A85` | Rotate clockwise |
| `0xFF9867` | Display my name ("ADON") on the LED panel |
| `0xFF6897` | Look left (servo) |
| `0xFFB04F` | Look right (servo) |

## Getting Started

1. Install the `IRremoteTank` library in the Arduino IDE.
2. Wire
