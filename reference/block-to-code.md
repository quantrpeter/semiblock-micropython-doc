# Block ↔ MicroPython code mapping

This table shows a representative block from each category alongside the MicroPython
code it generates. The output is pulled directly from `src/generators/micropython.js`
(field placeholders such as `var_name`, `pinNo`, etc. are shown as their literal
field names). Most blocks generate a single line; a few (DHT, HC-SR04, CSV, IoT)
emit several lines or pull in a driver class.

## Core / Machine

| Block `type` | Generated MicroPython |
| --- | --- |
| `createMainMethod` | Emits the standard header (`from machine import Pin, SoftI2C, ADC, PWM, UART`, `from time import sleep, sleep_ms, sleep_us`, `import network`, `import math`, …) followed by a `### start` marker and the body. Extra imports (`neopixel`, `ssd1306`, `_thread`, `servo`, `dht`, `sprite`, `urequests`) are added on demand. |
| `softReset` | `machine.soft_reset()` |
| `hardReset` | `machine.reset()` |
| `sleep` | `sleep(time)` |
| `sleep_ms` | `sleep_ms(time)` |
| `connectWifi` | `connectWifi("ssid", "password")` |
| `mem32Read` | `var_name = machine.mem32(address)` |
| `getCPUFreq` | `var_name = machine.freq()` |

## Language

| Block `type` | Generated MicroPython |
| --- | --- |
| `print` | `print(value)` |
| `variable` | `var_name = <statements>` |
| `comment` | `# comment` |
| `pass` | `pass` |
| `def` | `def funcName(parameters):` + indented body |
| `forLoop` | `for var1 in range(var2):` + indented body |
| `whileLoop` | `while conditions:` + indented body |
| `ifLoop` | `if conditions:` + indented body |
| `importCode` | `import libraryName` |
| `fromImportCode` | `from libraryName import component` |
| `startThread` | `varName = _thread.start_new_thread(funcName, ())` |

## Math

| Block `type` | Generated MicroPython |
| --- | --- |
| `mathAdd` | `A + B` |
| `mathMultiply` | `A * B` |
| `integerInit` | `value` |

## String

| Block `type` | Generated MicroPython |
| --- | --- |
| `stringUpper` | `value.upper()` |
| `stringReplace` | `value.replace(old, new)` |
| `stringSplit` | `value.split(delimiter)` |
| `stringLength` | `len(value)` |

## List

| Block `type` | Generated MicroPython |
| --- | --- |
| `createList` | `list_name = [list]` |
| `appendList` | `list_name.append(value)` |
| `sortList` | `list_name.sort()` |
| `getListSlice` | `var_name = list_name[start:end]` |

## Dictionary

| Block `type` | Generated MicroPython |
| --- | --- |
| `createDict` | `var_name = {}` |
| `dictSet` | `dict_name[key] = value` |
| `dictKeys` | `var_name = dict_name.keys()` |

## Random

| Block `type` | Generated MicroPython |
| --- | --- |
| `random` | `random.random()` |
| `randint` | `random.randint(A, B)` |
| `choice` | `random.choice(list)` |

## Regex / Requests

| Block `type` | Generated MicroPython |
| --- | --- |
| `reCompile` | `re.compile(pattern)` |
| `urequestsGet` | `urequests.get(url)` |
| `urequestsPost` | `urequests.post(url, data=data)` |

## SemiBlock IoT

| Block `type` | Generated MicroPython |
| --- | --- |
| `iotConnect` | `IOT_SERVER = "server"` / `IOT_DEVICE_ID = "device_id"` / `IOT_SECRET = "secret"` |
| `iotPushReading` | `urequests.post(IOT_SERVER + "/iot/data", json={"device_id": IOT_DEVICE_ID, "secret_key": IOT_SECRET, "sensor_type": "sensor_type", "data": data})` |

## OS / CSV

| Block `type` | Generated MicroPython |
| --- | --- |
| `csvRead` | Opens the file and appends each `csv.reader` row into `var_name`. |
| `csvAppend` | Opens the file in append mode and `csv.writer(...).writerow(data)`. |

## Display (SSD1306)

| Block `type` | Generated MicroPython |
| --- | --- |
| `ssd1306` | `display = ssd1306.SSD1306_I2C(width, height, SoftI2C(sda=Pin(sda), scl=Pin(scl)))` |
| `ssd1306_fill` | `display.fill(number)` |
| `ssd1306_show` | `display.show()` |
| `ssd1306_fillCircle` | `display.fill_circle(x, y, radius, 1)` |

## LVGL

| Block `type` | Generated MicroPython |
| --- | --- |
| `lvglInit` | `import lvgl as lv` |
| `lvglScreenCreate` | `screen_name = lv.obj()` |
| `lvglLabelCreate` | `label_name = lv.label(parent)` |
| `lvglLabelSetText` | `label_name.set_text("text")` |
| `lvglTaskHandler` | `lv.task_handler()` |

## Pin

| Block `type` | Generated MicroPython |
| --- | --- |
| `pin` | `var_name = Pin(pinNo, Pin.pinDirection)` |
| `on` | `var_name.on()` |
| `off` | `var_name.off()` |
| `uartInit` | `var_name = UART(uartNo, baudrate=baudrate, tx=tx, rx=rx)` |
| `neoPixel` | `var_name = neopixel.NeoPixel(Pin(pinNo, Pin.OUT), 1)` |
| `neoPixelWrite` | `var_name[0] = (r, g, b)` / `var_name.write()` |

## Timer / PWM / ADC

| Block `type` | Generated MicroPython |
| --- | --- |
| `timerInit` | `var_name = Timer(timer_id)` |
| `timerStart` | `var_name.init(period=period, mode=mode, callback=callback)` |
| `pwmInit` | `var_name = PWM(Pin(pin_number))` |
| `pwmSetDuty` | `var_name.duty(duty)` |
| `adcInit` | `var_name = ADC(Pin(pin_number))` |
| `adcRead` | `var_name = adc_name.read()` |

## SPI / I2C / One-Wire

| Block `type` | Generated MicroPython |
| --- | --- |
| `spiInit` | `var_name = SPI(spi_id, baudrate=…, polarity=…, phase=…, sck=Pin(sck), mosi=Pin(mosi), miso=Pin(miso))` |
| `i2cInit` | `var_name = I2C(i2c_id, scl=Pin(scl), sda=Pin(sda), freq=freq)` |
| `i2cScan` | `var_name = i2c_name.scan()` |
| `oneWireScan` | `var_name = ow_name.scan()` |

## Sensors

| Block `type` | Generated MicroPython |
| --- | --- |
| `temperature` | `var_name = getTemperature(D0, ADC)` |
| `servo` | `var_name = Servo(pin_number)` |
| `servoAngle` | `servo_Angle(var_name, angle)` |
| `motorOn` | `var_name (1)` |
| `dhtInit` | `var_name = dht.dht_type(Pin(pin))` |
| `dhtReadTemperature` | `dht_name.measure()` / `var_name = dht_name.temperature()` |
| `hcsr04Init` | Emits the full `HCSR04` driver class, then `var_name = HCSR04(trigger_pin=…, echo_pin=…, echo_timeout_us=…)` |
| `hcsr04DistanceCm` | `var_name = sonar_name.distance_cm()` |

## Generative AI / Open Data

| Block `type` | Generated MicroPython |
| --- | --- |
| `askDeepSeek` | `var_name = askDeepSeek("question")` |
| `getOpenDataTemperature` | `var_name = getOpenDataTemperature("location")` |
| `getBusArrivalTime` | `var_name = getBusArrivalTime(stopID, no)` |

---

**Next:** [Full block reference](blocks.md)
