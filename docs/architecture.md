# Firmware Architecture

## Overview

The firmware is a single-module keypad event loop written with Arduino APIs.

- File: `src/main.cpp`
- Main responsibilities:
  1. Define keypad matrix mapping.
  2. Define GPIO assignments for 12 LEDs.
  3. Initialize GPIO outputs in `setup()`.
  4. Poll keypad and execute LED actions in `loop()`.

## Module Structure

## 1) Constants and Tables

- `LEDS`, `ROWS`, `COLS`: dimensions and counts.
- `keys[ROWS][COLS]`: keypad character matrix.
- `ledPins[LEDS]`: logical LED index -> GPIO mapping.
- `rowPins[ROWS]` and `colPins[COLS]`: keypad wiring.

## 2) Keypad Driver Instance

- `Keypad keypad = Keypad(makeKeymap(...), rowPins, colPins, ROWS, COLS);`
- Handles matrix scanning and key decoding.

## 3) Initialization (`setup`)

- Iterates through all LED GPIOs.
- Sets each as output.
- Initializes all LEDs to OFF (`LOW`).

## 4) Runtime Loop (`loop`)

- Reads one key (`getKey()`).
- If a valid key is pressed (`NO_KEY` check), dispatches behavior via `switch`.
- Uses direct `digitalWrite` for individual LEDs and `for` loops for grouped actions.
- Ends with `delay(10)` to stabilize polling.

## Behavior Guarantees

- No behavior modifications were introduced.
- Key-to-action mapping is preserved exactly from provided source.
- Timing characteristic (`delay(10)`) is unchanged.

## Future Extension Points (Non-breaking)

- Extract key handlers into helper functions for readability.
- Add LED OFF behavior for `1..8`/`A..D` long-press variants.
- Add serial debug logging guarded by compile-time macro.
- Add Wi-Fi features in separate module with secrets isolated from source control.
