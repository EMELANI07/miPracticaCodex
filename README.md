# Raspberry Pi Pico W Keypad-to-LED Controller

A keypad-driven LED controller for **Raspberry Pi Pico W (RP2040)**.

This repository is cleaned and documented from the provided source and Wokwi hardware diagram, while preserving firmware behavior.

## Project Type and Framework

The provided firmware is **C/C++ using Arduino-style APIs** (`setup()`, `loop()`, `Keypad.h`).

- Target hardware: Raspberry Pi Pico W
- Recommended build/upload path: **Arduino IDE (Arduino-Pico core)** or **PlatformIO**
- Included: Pico-style repository structure with documentation
- Included `CMakeLists.txt`: structure placeholder for future Pico SDK migration

## Repository Structure

```text
.
├── CMakeLists.txt
├── include/
├── src/
│   └── main.cpp
├── docs/
│   ├── architecture.md
│   ├── wiring.md
│   └── wokwi/
│       └── diagram.json
└── README.md
```

## Features

- Reads a 4x4 matrix keypad (16 keys).
- Controls 12 LEDs mapped to keypad actions:
  - `1..8` turn on individual blue LEDs
  - `9` turns ON LEDs `1..8`
  - `0` turns OFF LEDs `1..8`
  - `A..D` turn on individual red LEDs
  - `*` turns ON red LEDs `A..D`
  - `#` turns OFF red LEDs `A..D`
- Maintains non-blocking polling loop (10 ms delay per cycle).

## Components (from diagram)

- 1x Raspberry Pi Pico / Pico W board
- 1x 4x4 membrane keypad
- 12x LEDs (8 blue + 4 red)
- 12x 220 Ω resistors (LED current limiting)
- 4x 1 kΩ resistors (keypad row pull-ups to 3V3)
- Jumper wires

## GPIO Mapping Summary

Detailed table is in [`docs/wiring.md`](docs/wiring.md).

- LEDs: GP11, GP10, GP9, GP8, GP7, GP6, GP5, GP4, GP3, GP2, GP28, GP27
- Keypad rows: GP26, GP22, GP21, GP20
- Keypad cols: GP19, GP18, GP17, GP16

## Build/Flash on Real Hardware

## Option A: Arduino IDE (recommended for current code)

1. Install Arduino IDE.
2. Install **Arduino-Pico** board package (Raspberry Pi Pico/RP2040 core).
3. Install `Keypad` library from Library Manager.
4. Select board: **Raspberry Pi Pico W**.
5. Open `src/main.cpp` (or copy content into an Arduino sketch).
6. Upload to Pico W.

## Option B: PlatformIO

1. Create a PlatformIO project for `raspberrypi` / Pico W with Arduino framework.
2. Place `src/main.cpp` in `src/`.
3. Add dependency `Keypad`.
4. Build and upload.

## Run in Wokwi

1. Create a new **Raspberry Pi Pico** project in Wokwi.
2. Replace the generated `diagram.json` with [`docs/wokwi/diagram.json`](docs/wokwi/diagram.json).
3. Use the C++/Arduino firmware from `src/main.cpp`.
4. Start simulation and press keypad buttons to observe LED behavior.

## Notes on Wi-Fi

- The current firmware does **not** use Pico W Wi-Fi.
- If Wi-Fi is added later, keep credentials in a separate local config file (excluded via `.gitignore`) and never hardcode secrets.

## Behavior Preservation

Core logic in `src/main.cpp` is preserved from the provided code; only repository organization and documentation were added.
