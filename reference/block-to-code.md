# Block ↔ MicroPython code mapping

This table shows a representative block from each category alongside the MicroPython
code it generates. The output is pulled directly from `src/generators/micropython.js`
(field placeholders such as `var_name`, `pinNo`, etc. are shown as their literal
field names). Most blocks generate a single line; a few (DHT, HC-SR04, CSV, IoT)
emit several lines or pull in a driver class.

## Core / Machine

> ![](hardblock/hardblock_Machine.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| `No Image` | `createMainMethod` | Emits the standard header (`from machine import Pin, SoftI2C, ADC, PWM, UART`, `from time import sleep, sleep_ms, sleep_us`, `import network`, `import math`, …) followed by a `### start` marker and the body. Extra imports (`neopixel`, `ssd1306`, `_thread`, `servo`, `dht`, `sprite`, `urequests`) are added on demand. |
| ![](block/machine1.png){width=inherit} | `softReset` | `machine.soft_reset()` |
| ![](block/machine2.png){width=inherit} | `hardReset` | `machine.reset()` |
| ![](block/machine3.png){width=inherit} | `sleep` | `sleep(time)` |
| ![](block/machine4.png){width=inherit} | `sleep_ms` | `sleep_ms(time)` |
| ![](block/machine5.png){width=inherit} | `connectWifi` | `connectWifi("ssid", "password")` |
| ![](block/machine6.png){width=inherit} | `mem32Read` | `var_name = machine.mem32(address)` |
| ![](block/machine7.png){width=inherit} | `getCPUFreq` | `var_name = machine.freq()` |

## Language

> ![](hardblock/hardblock_Language.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/lang1.png){width=inherit} | `print` | `print(value)` |
| ![](block/lang2.png){width=inherit} | `variable` | `var_name = <statements>` |
| ![](block/lang3.png){width=inherit} | `comment` | `# comment` |
| ![](block/lang4.png){width=inherit} | `pass` | `pass` |
| ![](block/lang5.png){width=inherit} | `def` | `def funcName(parameters):` + indented body |
| ![](block/lang6.png){width=inherit} | `forLoop` | `for var1 in range(var2):` + indented body |
| ![](block/lang7.png){width=inherit} | `whileLoop` | `while conditions:` + indented body |
| ![](block/lang8.png){width=inherit} | `ifLoop` | `if conditions:` + indented body |
| ![](block/lang9.png){width=inherit} | `importCode` | `import libraryName` |
| ![](block/lang10.png){width=inherit} | `fromImportCode` | `from libraryName import component` |
| ![](block/lang11.png){width=inherit} | `startThread` | `varName = _thread.start_new_thread(funcName, ())` |

## Math

> ![](hardblock/hardblock_Math.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/math1.png){width=inherit} | `mathNumber` | `value` |
| ![](block/math2.png){width=inherit} | `mathAdd` | `A + B` |
| ![](block/math3.png){width=inherit} | `mathSubtract` | `A - B` |
| ![](block/math4.png){width=inherit} | `mathMultiply` | `A * B` |
| ![](block/math5.png){width=inherit} | `mathDivide` | `A / B` |
| ![](block/math6.png){width=inherit} | `mathModulo` | `A % B` |
| ![](block/math7.png){width=inherit} | `mathPower` | `A ** B` |
| ![](block/math8.png){width=inherit} | `mathSqrt` | `math.sqrt(A)` |
| ![](block/math9.png){width=inherit} | `mathSin` | `math.sin(A)` |
| ![](block/math10.png){width=inherit} | `mathCos` | `math.cos(A)` |
| ![](block/math11.png){width=inherit} | `mathTan` | `math.tan(A)` |
| ![](block/math12.png){width=inherit} | `mathLog` | `math.log(A)` |
| ![](block/math13.png){width=inherit} | `mathExp` | `math.exp(A)` |
| ![](block/math14.png){width=inherit} | `mathAbs` | `abs(A)` |
| ![](block/math15.png){width=inherit} | `mathFloor` | `math.floor(A)` |
| ![](block/math16.png){width=inherit} | `mathCeil` | `math.ceil(A)` |
| ![](block/math17.png){width=inherit} | `mathRound` | `round(A)` |
| ![](block/math18.png){width=inherit} | `mathMin` | `min(A, B)` |
| ![](block/math19.png){width=inherit} | `mathMax` | `max(A, B)` |
| ![](block/math20.png){width=inherit} | `mathPi` | `math.pi` |
| ![](block/math21.png){width=inherit} | `mathE` | `math.e` |
| ![](block/math22.png){width=inherit} | `mathRandom` | `random.random()` |
| ![](block/math23.png){width=inherit} | `mathRandint` | `random.randint(A, B)` |
| ![](block/math24.png){width=inherit} | `mathDivmod` | `divmod(A, B)` |
| ![](block/math25.png){width=inherit} | `mathHex` | `hex(A)` |
| ![](block/math26.png){width=inherit} | `mathOrd` | `ord(A)` |

## String

> ![](hardblock/hardblock_String.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/string1.png){width=inherit} | `stringText` | `'text'` |
| ![](block/string2.png){width=inherit} | `stringUpper` | `text.upper()` |
| ![](block/string3.png){width=inherit} | `stringLower` | `TEXT.lower()` |
| ![](block/string4.png){width=inherit} | `stringStrip` | `text.strip()` |
| ![](block/string5.png){width=inherit} | `stringReplace` | `text.replace('t', 'T')` |
| ![](block/string6.png){width=inherit} | `stringFind` | `text.find('t')` |
| ![](block/string7.png){width=inherit} | `stringSplit` | `'a,b,c'.split(',')` |
| ![](block/string8.png){width=inherit} | `stringJoin` | `','.join(['a', 'b', 'c'])` |
| ![](block/string9.png){width=inherit} | `stringStartswith` | `text.startswith('t')` |
| ![](block/string10.png){width=inherit} | `stringEndswith` | `text.endswith('t')` |
| ![](block/string11.png){width=inherit} | `stringLen` | `len(text)` |
| ![](block/string12.png){width=inherit} | `stringInsertNewlineEveryNChars` | `'\n'.join([s[i:i+4] for i in range(0, len(s), 4)])` |
| ![](block/string13.png){width=inherit} | `stringAdd` | `'abc' + 'def'` |

## List

> ![](hardblock/hardblock_List.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/list1.png){width=inherit} | `listInit` | `list1 = [20, 50, 30]` |
| ![](block/list2.png){width=inherit} | `listAppend` | `list1.append(10)` |
| ![](block/list3.png){width=inherit} | `listInsert` | `list1.insert(0, 10)` |
| ![](block/list4.png){width=inherit} | `listRemove` | `list1.remove(10)` |
| ![](block/list5.png){width=inherit} | `listPop` | `list1.pop(-1)` |
| ![](block/list6.png){width=inherit} | `listSort` | `list1.sort()` |
| ![](block/list7.png){width=inherit} | `listReverse` | `list1.reverse()` |
| ![](block/list8.png){width=inherit} | `listLen` | `length = len(list1)` |
| ![](block/list9.png){width=inherit} | `listItem` | `item = list1[0]` |
| ![](block/list10.png){width=inherit} | `listSliceStartEnd` | `slice = list1[0:2]` |
| ![](block/list11.png){width=inherit} | `listSliceEnd` | `slice = list1[:2]` |
| ![](block/list12.png){width=inherit} | `listSliceStart` | `slice = list1[0:]` |
| ![](block/list13.png){width=inherit} | `listSliceCopy` | `slice = list1[:]` |

## Dictionary

> ![](hardblock/hardblock_Dict.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/dict1.png){width=inherit} | `dictInit` | `dict1 = {}` |
| ![](block/dict2.png){width=inherit} | `dictSet` | `dict1['key1'] = value1` |
| ![](block/dict3.png){width=inherit} | `dictGet` | `value = dict1['key1']` |
| ![](block/dict4.png){width=inherit} | `dictKeys` | `keys = dict1.keys()` |
| ![](block/dict5.png){width=inherit} | `dictValues` | `values = dict1.values()` |
| ![](block/dict6.png){width=inherit} | `dictItems` | `items = dict1.items()` |
| ![](block/dict7.png){width=inherit} | `dictPop` | `value = dict1.pop('key1')` |
| ![](block/dict8.png){width=inherit} | `dictUpdate` | `dict1.update(dict2)` |
| ![](block/dict9.png){width=inherit} | `dictClear` | `dict1.clear()` |

## Random

> ![](hardblock/hardblock_Random.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/ran1.png){width=inherit} | `randomRandom` | `random.random()` |
| ![](block/ran2.png){width=inherit} | `randomRandint` | `random.randint(A, B)` |
| ![](block/ran3.png){width=inherit} | `randomChoice` | `random.choice(A)` |
| ![](block/ran4.png){width=inherit} | `randomShuffle` | `random.shuffle(A)` |
| ![](block/ran5.png){width=inherit} | `randomUniform` | `random.uniform(A, B)` |
| ![](block/ran6.png){width=inherit} | `randomRandrange` | `random.randrange(A, B, C)` |
| ![](block/ran7.png){width=inherit} | `randomSample` | `random.sample(A, B)` |

## Regex / Requests

> ![](hardblock/hardblock_Regex.png){width=inherit} ![](hardblock/hardblock_Req.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/req1.png){width=inherit} | `reMatch` | `result = re.match(pattern, string)` |
| ![](block/req2.png){width=inherit} | `reSearch` | `result = re.search(pattern, string)` |
| ![](block/req3.png){width=inherit} | `reFindall` | `result = re.findall(pattern, string)` |
| ![](block/req4.png){width=inherit} | `reFinditer` | `result = re.finditer(pattern, string)` |
| ![](block/req5.png){width=inherit} | `reSub` | `result = re.sub(pattern, replacement, string)` |
| ![](block/req6.png){width=inherit} | `reSplit` | `result = re.split(pattern, string)` |
| ![](block/req7.png){width=inherit} | `reCompile` | `compiled_pattern = re.compile(pattern)` |
| ![](block/req8.png){width=inherit} | `urequestsGet` | `response = urequests.get('http://example.com')` |
| ![](block/req9.png){width=inherit} | `urequestsJson` | `data = response.json()` |
| ![](block/req10.png){width=inherit} | `urequestsPost` | `response = urequests.post('http://example.com', {"key": "value"})` |
| ![](block/req11.png){width=inherit} | `urequestsPut` | `response = urequests.put('http://example.com', {"key": "value"})` |
| ![](block/req12.png){width=inherit} | `urequestsDelete` | `response = urequests.delete('http://example.com')` |
| ![](block/req13.png){width=inherit} | `urequestsHead` | `response = urequests.head('http://example.com')` |


## SemiBlock IoT

> ![](hardblock/hardblock_IoT.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/iot1.png){width=inherit} | `iotConnect` | `IOT_SERVER = "https://build.semiblock.ai"` / `IOT_DEVICE_ID = "device_id"` / `IOT_SECRET = "secret"` |
| ![](block/iot2.png){width=inherit} | `iotPushReading` | `urequests.post(IOT_SERVER + "/iot/data", json={"device_id": IOT_DEVICE_ID, "secret_key": IOT_SECRET, "sensor_type": "dht11", "data": {"temperature": 24, "humidity": 60}})` |
| ![](block/iot3.png){width=inherit} | `iotPushSingleValue` | `urequests.post(IOT_SERVER + "/iot/data", json={"device_id": IOT_DEVICE_ID, "secret_key": IOT_SECRET, "sensor_type": "thermometer", "data": {"temperature": temp}})` |

## OS / CSV

> ![](hardblock/hardblock_OS.png){width=inherit} ![](hardblock/hardblock_CSV.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/os1.png){width=inherit} | `csvRead` | `data = read_csv('file.csv')` |
| ![](block/os2.png){width=inherit} | `csvWrite` | `write_csv('file.csv', [["col1", "col2"], ["val1", "val2"]])` |
| ![](block/os3.png){width=inherit} | `csvAppend` | `append_csv('file.csv', ["val1", "val2"])` |
| ![](block/os4.png){width=inherit} | `osListdir` | `os.listdir('/')` |
| ![](block/os5.png){width=inherit} | `osRemove` | `os.remove('/file.txt')` |
| ![](block/os6.png){width=inherit} | `osRename` | `os.rename('/old.txt', '/new.txt')` |
| ![](block/os7.png){width=inherit} | `osMkdir` | `os.mkdir('/new_folder')` |
| ![](block/os8.png){width=inherit} | `osRmdir` | `os.rmdir('/folder')` |
| ![](block/os9.png){width=inherit} | `osGetcwd` | `os.getcwd()` |
| ![](block/os10.png){width=inherit} | `osChdir` | `os.chdir('/new_folder')` |
| ![](block/os11.png){width=inherit} | `osStat` | `os.stat('/file.txt')` |
| ![](block/os12.png){width=inherit} | `osUname` | `os.uname()` |
| ![](block/os13.png){width=inherit} | `osSync` | `os.sync()` |
| ![](block/os14.png){width=inherit} | `osSystem` | `os.system('ls')` |
| ![](block/os15.png){width=inherit} | `osUrandom` | `os.urandom(16)` |

## Display (SSD1306)

> ![](hardblock/hardblock_Display.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/dis1.png){width=inherit} | `ssd1306` | `display = ssd1306.SSD1306_I2C(128, 64, SoftI2C(sda=Pin(10), scl=Pin(10)))` |
| ![](block/dis2.png){width=inherit} | `ssd1306_fill` | `display.fill(0)` |
| ![](block/dis3.png){width=inherit} | `ssd1306_show` | `display.show()` |
| ![](block/dis4.png){width=inherit} | `ssd1306_contrast` | `display.contrast(255)` |
| ![](block/dis5.png){width=inherit} | `ssd1306_invert` | `display.invert(0)` |
| ![](block/dis6.png){width=inherit} | `ssd1306_rotate` | `display.rotate(True)` |
| ![](block/dis7.png){width=inherit} | `ssd1306_text` | `display.text("Helloworld", 0, 0)` |
| ![](block/dis8.png){width=inherit} | `ssd1306_pixel` | `display.pixel(0, 0, 1)` |
| ![](block/dis9.png){width=inherit} | `ssd1306_hline` | `display.hline(0, 0, 4, 1)` |
| ![](block/dis10.png){width=inherit} | `ssd1306_vline` | `display.vline(0, 0, 4, 1)` |
| ![](block/dis11.png){width=inherit} | `ssd1306_line` | `display.line(0, 0, 100, 100, 1)` |
| ![](block/dis12.png){width=inherit} | `ssd1306_rect` | `display.rect(0, 0, 100, 50, 1)` |
| ![](block/dis13.png){width=inherit} | `ssd1306_fill_rect` | `display.fill_rect(0, 0, 100, 50, 1)` |
| ![](block/dis14.png){width=inherit} | `ssd1306_circle` | `display.circle(64, 32, 10, 1)` |
| ![](block/dis15.png){width=inherit} | `ssd1306_fillCircle` | `display.fill_circle(64, 32, 10, 1)` |
| ![](block/dis16.png){width=inherit} | `ssd1306_scroll` | `display.scroll(10, 0)` |
| ![](block/dis17.png){width=inherit} | `display_create_image` | `image = bytearray([...])` |
| ![](block/dis18.png){width=inherit} | `display_draw_pixels` | `display.blit(image, 0, 0)` |
| ![](block/dis19.png){width=inherit} | `display_setColor` | `display.setColor('Red')` |
| ![](block/dis20.png){width=inherit} | `display_setFontSize` | `display.setFontSize(10)` |

## LVGL

| Block `type` | Generated MicroPython |
| --- | --- |
| `lvglInit` | `import lvgl as lv` |
| `lvglScreenCreate` | `screen_name = lv.obj()` |
| `lvglLabelCreate` | `label_name = lv.label(parent)` |
| `lvglLabelSetText` | `label_name.set_text("text")` |
| `lvglTaskHandler` | `lv.task_handler()` |

## Pin

> ![](hardblock/hardblock_Pin.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/pin1.png){width=inherit} | `pinInitOut` | `p0 = Pin(0, OUT)` |
| ![](block/pin2.png){width=inherit} | `pinInitIn` | `p0 = Pin(0, IN, PULL_UP)` |
| ![](block/pin3.png){width=inherit} | `pinOn` | `p0.on()` |
| ![](block/pin4.png){width=inherit} | `pinOff` | `p0.off()` |
| ![](block/pin5.png){width=inherit} | `pinValue` | `var1 = p0.value()` |
| ![](block/pin6.png){width=inherit} | `uartInit` | `var1 = UART(0, baudrate=9600, tx=16, rx=17)` |
| ![](block/pin7.png){width=inherit} | `uartRead` | `var1.read(8)` |
| ![](block/pin8.png){width=inherit} | `uartWrite` | `var1.write('hello')` |
| ![](block/pin9.png){width=inherit} | `neopixelInit` | `pixel = neopixel.NeoPixel(Pin(8, Pin.OUT), 1)` |
| ![](block/pin10.png){width=inherit} | `neopixelSetWrite` | `pixel[0] = (0xff, 0xff, 0xff)`<br>`pixels.write()` |

## Timer / PWM / ADC

> ![](hardblock/hardblock_Timer.png){width=inherit} ![](hardblock/hardblock_PWM.png){width=inherit} ![](hardblock/hardblock_ADC.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](block/mach1.png){width=inherit} | `timerInit` | `timer1 = Timer(0)` |
| ![](block/mach2.png){width=inherit} | `timerConfig` | `timer1.init(period=1000, mode=Timer.ONE_SHOT, callback=callback_function)` |
| ![](block/mach3.png){width=inherit} | `timerDeinit` | `timer1.deinit()` |
| ![](block/mach4.png){width=inherit} | `pwmInit` | `pwm1 = PWM(Pin(15))` |
| ![](block/mach5.png){width=inherit} | `pwmFreq` | `pwm1.freq(1000)` |
| ![](block/mach6.png){width=inherit} | `pwmDuty` | `pwm1.duty(512)` |
| ![](block/mach7.png){width=inherit} | `pwmDeinit` | `pwm1.deinit()` |
| ![](block/mach8.png){width=inherit} | `adcInit` | `adc1 = ADC(Pin(32))` |
| ![](block/mach9.png){width=inherit} | `adcRead` | `value = adc1.read()` |
| ![](block/mach10.png){width=inherit} | `dacInit` | `dac1 = DAC(Pin(25))` |
| ![](block/mach11.png){width=inherit} | `dacWrite` | `dac1.write(128)` |

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

