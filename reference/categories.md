# Category color legend

Every category in the SemiBlock toolbox is tinted with a colour defined in the
`categoryStyles` object in `src/index.js`. The toolbar groups the categories with
three separators — **Python**, **Hardware Blocks**, and **Sensor & AI Blocks** — and
the tables below follow that same grouping.

The colour hex values are transcribed directly from the `categoryStyles` object; the
icon for each category is rendered in a darker shade (about −30 %) of the same colour.

## Core / Sprite blocks (before the *Python* separator)

| Category | Style key | Colour |
| --- | --- | --- |
| Machine | `machine_category` | `#a2d2ff` |
| Motion | `motion_category` | `#4C97FF` |
| Looks | `looks_category` | `#9966FF` |
| Events | `events_category` | `#FFBF00` |
| Waveshare 3.5 | `machine_category` | `#a2d2ff` |

## Python blocks (after the *Python* separator)

| Category | Style key | Colour |
| --- | --- | --- |
| Language | `language_category` | `#fb6f92` |
| List | `list_category` | `#ff8fab` |
| Dictionary | `dictionary_category` | `#ffb3c6` |
| Math | `math_category` | `#ffc2d1` |
| String | `string_category` | `#ffe5ec` |
| Random | `random_category` | `#ff8500` |
| Exception | `exception_category` | `#ff9100` |
| Regex | `regex_category` | `#ff9e00` |
| Requests | `requests_category` | `#ffaa00` |
| SemiBlock IoT | `semiblockIot_category` | `#6c5ce7` |
| CSV | `csv_category` | `#4ad66d` |
| OS | `os_category` | `#6ede8a` |
| Display | `display_category` | `#92e6a7` |
| LVGL | `lvgl_category` | `#b8f5c7` |

## Hardware blocks (after the *Hardware Blocks* separator)

| Category | Style key | Colour |
| --- | --- | --- |
| Pin | `pin_category` | `#00b4d8` |
| Timer | `timer_category` | `#48cae4` |
| PWM | `pwm_category` | `#90e0ef` |
| ADC | `adc_category` | `#ade8f4` |
| SPI | `spi_category` | `#fb6f92` |
| I2C | `i2c_category` | `#ff8fab` |
| WatchDog | `watchdog_category` | `#ffb3c6` |
| SD Card | `sdcard_category` | `#ffc2d1` |
| RMT | `rmt_category` | `#ff8500` |
| One-Wire | `onewire_category` | `#ff9100` |
| Capacitive Touch | `capacitiveTouch_category` | `#ff9e00` |
| DHT | `dht_category` | `#ffaa00` |
| HC-SR04 Sonar | `sonar_category` | `#ffb700` |

## Sensor & AI blocks (after the *Sensor & AI Blocks* separator)

| Category | Style key | Colour |
| --- | --- | --- |
| Sensors | `sensors_category` | `#4ad66d` |
| Generative AI | `gai_category` | `#6ede8a` |
| Open Data | `openData_category` | `#92e6a7` |

## Additional style keys

The `categoryStyles` object also defines `sprite_category` (`#4C97FF`), used by the
Scratch-style sprite blocks. It shares its colour with the **Motion** category.

---

**Next:** [Save / Load file format](workspace-format.md)
