# Wiring and GPIO Mapping (Raspberry Pi Pico W)

This wiring documentation is derived from the provided Wokwi `diagram.json`.

## Assumptions and Notes

- Diagram part is `wokwi-pi-pico`; pinout is compatible with Pico W GPIO for this project.
- LED cathodes are tied to common GND.
- Each LED anode is driven from a GPIO through a 220 Ω resistor.
- Keypad rows are connected to GPIO and also pulled up to 3V3 with 1 kΩ resistors.

## Keypad Connections

| Keypad Pin | Pico GPIO |
|---|---|
| C1 | GP19 |
| C2 | GP18 |
| C3 | GP17 |
| C4 | GP16 |
| R1 | GP26 |
| R2 | GP22 |
| R3 | GP21 |
| R4 | GP20 |

## LED Connections

> Firmware order in `ledPins[]`: `{11,10,9,8,7,6,5,4,3,2,28,27}`

| Logical LED | Label in Diagram | Pico GPIO | Resistor |
|---|---|---|---|
| LED1 | `1` (blue) | GP11 | 220 Ω |
| LED2 | `2` (blue) | GP10 | 220 Ω |
| LED3 | `3` (blue) | GP9  | 220 Ω |
| LED4 | `4` (blue) | GP8  | 220 Ω |
| LED5 | `5` (blue) | GP7  | 220 Ω |
| LED6 | `6` (blue) | GP6  | 220 Ω |
| LED7 | `7` (blue) | GP5  | 220 Ω |
| LED8 | `8` (blue) | GP4  | 220 Ω |
| LED9 | `A` (red)  | GP3  | 220 Ω |
| LED10 | `B` (red) | GP2  | 220 Ω |
| LED11 | `C` (red) | GP28 | 220 Ω |
| LED12 | `D` (red) | GP27 | 220 Ω |

## Power and Ground

- Keypad pull-up network: 3V3 -> four 1 kΩ resistors -> R1/R2/R3/R4 lines.
- All LED cathodes are connected to Pico GND.

## Functional Mapping

- Keys `1..8`: turn ON individual blue LEDs.
- Key `9`: turns ON all blue LEDs.
- Key `0`: turns OFF all blue LEDs.
- Keys `A..D`: turn ON individual red LEDs.
- Key `*`: turns ON all red LEDs.
- Key `#`: turns OFF all red LEDs.
