# Project: Distance Alarm (HC-SR04 + NeoPixel)

A proximity alarm: an **HC-SR04** ultrasonic sensor measures how far away an
object is, and a **NeoPixel** RGB LED changes colour — green when clear, yellow
when close, red when something is too near.

## What you'll build

- An **HC-SR04** sonar reading distance in centimetres.
- A **NeoPixel** (WS2812) LED that turns **green → yellow → red** as the object
  approaches.
- A loop that reads distance and recolours the LED several times a second.

## Parts needed / wiring

| Part | Connect to ESP32 |
| --- | --- |
| HC-SR04 Trig | GPIO **5** |
| HC-SR04 Echo | GPIO **18** |
| HC-SR04 VCC / GND | 5V / GND |
| NeoPixel DIN | GPIO **13** |
| NeoPixel VCC / GND | 3V3 / GND |

> The HC-SR04 echo line is 5 V. Many ESP32 boards tolerate it on input, but a
> simple resistor divider on Echo is safer for long-term use.

## Blocks used (which categories)

- **Sensors → HC-SR04**: `hcsr04Init`, `hcsr04DistanceCm` — see
  [../sensors/hc-sr04.md](../sensors/hc-sr04.md).
- **Hardware → NeoPixel**: `neoPixel`, `neoPixelWrite` — see
  [../hardware/pin/neopixel.md](../hardware/pin/neopixel.md).
- **Logic / Loops**: a `while` loop, `if / elif / else`, and `sleep_ms`.

## Step-by-step block assembly

1. From **HC-SR04**, drag **`init sonar sonar trigger 5 echo 18`**. This block
   also drops in the HCSR04 driver class for you.
2. From **NeoPixel**, drag **`init NeoPixel np on pin 13`**.
3. Add a forever **`while True`** loop.
4. Inside, place **`read sonar sonar distance cm into dist`**.
5. Add an **`if / elif / else`**:
   - `dist > 30` → set NeoPixel to **green** `(0, 64, 0)`.
   - `dist > 10` → set NeoPixel to **yellow** `(64, 48, 0)`.
   - else → set NeoPixel to **red** `(64, 0, 0)`.
6. End the loop with **`sleep 100 ms`**.

## Full generated MicroPython

```python
from machine import Pin, SoftI2C, ADC, PWM, UART
from time import sleep, sleep_ms, sleep_us
import network
import math
import neopixel

### start

import machine
from machine import Pin
from utime import sleep_us

class HCSR04:
    def __init__(self, trigger_pin, echo_pin, echo_timeout_us=500*2*30):
        self.echo_timeout_us = echo_timeout_us
        self.trigger = Pin(trigger_pin, mode=Pin.OUT, pull=None)
        self.trigger.value(0)
        self.echo = Pin(echo_pin, mode=Pin.IN, pull=None)
    def _send_pulse_and_wait(self):
        self.trigger.value(0)
        sleep_us(5)
        self.trigger.value(1)
        sleep_us(10)
        self.trigger.value(0)
        try:
            pulse_time = machine.time_pulse_us(self.echo, 1, self.echo_timeout_us)
            if pulse_time < 0:
                pulse_time = int(500 * 29.1)
            return pulse_time
        except OSError as ex:
            if ex.args[0] == 110:
                raise OSError("Out of range")
            raise ex
    def distance_mm(self):
        pulse_time = self._send_pulse_and_wait()
        return pulse_time * 100 // 582
    def distance_cm(self):
        pulse_time = self._send_pulse_and_wait()
        return (pulse_time / 2) / 29.1

sonar = HCSR04(trigger_pin=5, echo_pin=18, echo_timeout_us=30000)
np = neopixel.NeoPixel(Pin(13, Pin.OUT), 1)
while True:
    dist = sonar.distance_cm()
    if dist > 30:
        np[0] = (0, 64, 0)
        np.write()
    elif dist > 10:
        np[0] = (64, 48, 0)
        np.write()
    else:
        np[0] = (64, 0, 0)
        np.write()
    sleep_ms(100)
```

> The `init sonar` block emits the whole `HCSR04` class plus the constructor
> line. `import neopixel` is added automatically because a NeoPixel block is used.

## How to run

1. Build the blocks and press **Run**.
2. Wave your hand toward the sensor: the LED should move green → yellow → red.
3. If the colour never changes, print `dist` to confirm the sensor returns sane
   centimetre values (2–400 cm typical).

## Extensions / challenges

- **Buzzer beeps:** add a PWM buzzer whose beep rate speeds up as `dist` drops.
- **Smooth fade:** map `dist` directly to a red/green mix instead of 3 steps.
- **Parking helper:** hold red steady once `dist` is below a "stop" threshold.
- **Multi-pixel bar:** use a NeoPixel strip and light more pixels as things near.

---

**Next:** [Project: Mini Dashboard (LVGL + chart + WiFi)](lvgl-dashboard.md)
