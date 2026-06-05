# Project: Mini Dashboard (LVGL + chart + WiFi)

Build a live on-device dashboard with **LVGL**: a line **chart** plus a text
**label** that update from a sensor reading. The same pattern works whether the
value comes from a local sensor or is fetched over **Wi-Fi**.

## What you'll build

- An **LVGL** screen with a **chart** (scrolling line graph) and a **label**
  showing the latest value.
- A loop that reads a value (here a temperature reading), pushes it into the
  chart, and updates the label text.
- Wi-Fi connectivity so the value can later come from a web request.

## Parts needed / wiring

| Part | Connect to ESP32 |
| --- | --- |
| SPI/I²C LCD running LVGL | per your panel's driver (see LVGL drivers) |
| DHT22 data (sample source) | GPIO **15** |

> LVGL needs a display driver initialised for your panel. See
> [../display/lvgl/drivers.md](../display/lvgl/drivers.md) and
> [../display/lvgl/init.md](../display/lvgl/init.md).

## Blocks used (which categories)

- **Network**: `connectWifi` — join Wi-Fi at startup.
- **Display → LVGL → Init/Screens**: `lvglInit`, `lvglScreenCreate`,
  `lvglScreenLoad` — see [../display/lvgl/screens.md](../display/lvgl/screens.md).
- **Display → LVGL → Data widgets**: `lvglChartCreate`, `lvglChartAddSeries`,
  `lvglChartSetPoint` — see
  [../display/lvgl/widgets-data.md](../display/lvgl/widgets-data.md).
- **Display → LVGL → Basic widgets**: `lvglLabelCreate`, `lvglLabelSetText` —
  see [../display/lvgl/widgets-basic.md](../display/lvgl/widgets-basic.md).
- **Display → LVGL → Tick**: `lvglTaskHandler` — see
  [../display/lvgl/tick.md](../display/lvgl/tick.md).
- **Sensors → DHT**: `dhtInit`, `dhtReadTemperature` — see
  [../sensors/dht.md](../sensors/dht.md).

## Step-by-step block assembly

1. Add **`connect WiFi`** with your credentials.
2. Add **`LVGL init`**, then **`create screen scr`** and **`load screen scr`**.
3. From data widgets, add **`create chart chart on scr`**, set its size, then
   **`add series series to chart colour 0x00FF00`**.
4. From basic widgets, add **`create label label on scr`** and position it.
5. Add the **`init DHT22 sensor on pin 15`** block.
6. Start a **`while True`** loop:
   - **`read DHT22 sensor temperature into temp`**.
   - **`set next chart value series = temp`**.
   - **`set label text`** to the latest reading.
   - **`LVGL task handler`** to redraw.
   - **`sleep_ms 500`**.

## Full generated MicroPython

```python
from machine import Pin, SoftI2C, ADC, PWM, UART
from time import sleep, sleep_ms, sleep_us
import network
import math

import dht

### start

connectWifi("MyWiFi", "MyPassword")
import lvgl as lv
scr = lv.obj()
lv.scr_load(scr)
chart = lv.chart(scr)
chart.set_size(200, 120)
chart.align(lv.ALIGN.CENTER, 0, -10)
series = chart.add_series(lv.color_hex(0x00FF00), lv.chart.AXIS.PRIMARY_Y)
label = lv.label(scr)
label.align(lv.ALIGN.BOTTOM_MID, 0, -5)
label.set_text("Starting...")
sensor = dht.DHT22(Pin(15))
while True:
    sensor.measure()
    temp = sensor.temperature()
    chart.set_next_value(series, temp)
    label.set_text("Temp: " + str(temp) + " C")
    lv.task_handler()
    sleep_ms(500)
```

> The LVGL blocks emit `lv.obj()`, `lv.chart(scr)`,
> `chart.add_series(lv.color_hex(0x00FF00), lv.chart.AXIS.PRIMARY_Y)` and
> `chart.set_next_value(series, temp)` exactly as shown. `import dht` is added
> automatically because the DHT block is used.

## How to run

1. Make sure your LVGL display driver is configured for your panel first.
2. Build the blocks and press **Run**. The chart line should grow with each
   reading and the label should track the latest temperature.
3. Nothing on screen? Confirm `lv.task_handler()` runs inside the loop — LVGL
   only redraws when the handler is called.

## Extensions / challenges

- **Fetch over Wi-Fi:** replace the DHT read with a web request (e.g. open-data
  temperature) so the chart plots a remote value.
- **Two series:** add a second `add series` for humidity in a different colour.
- **Range labels:** add min/max labels above and below the chart.
- **Touch to pause:** add a button widget that freezes updates when tapped.

---

**Next:** [Project: AI Voice Assistant (DeepSeek + LVGL)](ai-assistant.md)
