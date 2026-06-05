# Project: Smart Desk Lamp (PWM + Touch)

A desk lamp whose brightness you control by touching a wire. A capacitive
**Touch** input reads how strongly you press, and a **PWM** signal dims an LED
(or a small LED module) smoothly from off to full brightness.

## What you'll build

- A single LED driven by **PWM** so it can be any brightness, not just on/off.
- A **Touch** pad (a jumper wire or copper tape) that acts as a slider: the
  longer/harder you touch, the brighter the lamp.
- A loop that reads the touch value, converts it to a duty cycle, and updates
  the LED every fraction of a second.

## Parts needed / wiring

| Part | Connect to ESP32 |
| --- | --- |
| LED (+ 220 Ω resistor) | GPIO **2** → resistor → LED → GND |
| Touch wire / pad | GPIO **4** (a touch-capable pin) |

> Touch-capable pins on the ESP32 include GPIO 4, 13, 14, 15, 27, 32, 33.
> A **lower** `read()` value means a **stronger** touch.

## Blocks used (which categories)

- **Hardware → PWM**: `pwmInit`, `pwmSetFreq`, `pwmSetDuty` — see
  [../hardware/pwm/api.md](../hardware/pwm/api.md) and
  [../hardware/pwm/led-dim.md](../hardware/pwm/led-dim.md).
- **Hardware → Touch**: `touchInit`, `touchRead` — see
  [../hardware/touch/api.md](../hardware/touch/api.md).
- **Logic / Loops**: a forever `while` loop, a variable, and `sleep_ms`.

## Step-by-step block assembly

1. From **PWM**, drag **`init PWM led on pin 2`**. This creates the LED output.
2. Add **`set led frequency to 1000`** so the LED flickers far above what the
   eye can see.
3. From **Touch**, drag **`init touch touch on pin 4`**.
4. Add a forever **`while True`** loop.
5. Inside the loop, place **`read touch touch into value`**.
6. Add a variable block: `duty = (1023 - value) * 4`. As touch grows, `value`
   drops, so `duty` (0–1023 range for `.duty()`) grows — brighter lamp.
7. From **PWM**, add **`set led duty to duty`**.
8. Finish with **`sleep 50 ms`** to pace the loop.

## Full generated MicroPython

```python
from machine import Pin, SoftI2C, ADC, PWM, UART
from time import sleep, sleep_ms, sleep_us
import network
import math

### start

led = PWM(Pin(2))
led.freq(1000)
touch = TouchPad(Pin(4))
while True:
    value = touch.read()
    duty = (1023 - value) * 4
    if duty < 0:
        duty = 0
    if duty > 1023:
        duty = 1023
    led.duty(duty)
    sleep_ms(50)
```

> The PWM/Touch blocks emit `PWM(Pin(2))` and `TouchPad(Pin(4))` exactly as
> shown. `TouchPad` is provided by the SemiBlock firmware's `machine` module; on
> stock MicroPython add `from machine import TouchPad` at the top.

## How to run

1. Connect the board and open the SemiBlock MicroPython editor.
2. Build the blocks above, then press **Run** (or flash `main.py`).
3. Touch the wire on GPIO 4 and watch the lamp brighten. Release to dim.
4. If the lamp is always full/always off, print `value` first to learn the
   touched vs. untouched range on your board, then adjust the `duty` formula.

## Extensions / challenges

- **Calibrate automatically:** at start, read `touch.read()` a few times with no
  finger to learn the "released" baseline, then map relative to it.
- **Two-zone dimmer:** add a second touch pad to set a *minimum* brightness.
- **Night mode:** combine with a temperature or light reading so the lamp caps
  its maximum brightness in the evening.
- **Breathing effect:** when untouched, slowly ramp `duty` up and down for a
  gentle pulse using a counter variable.

---

**Next:** [Project: Weather Station (DHT + OLED + IoT push)](weather-station.md)
