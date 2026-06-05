# Real-Time Clock (RTC)

The **RTC** keeps the current date and time. On the ESP32 it also keeps running
during deep sleep, so it is handy for timestamps and scheduling.

The `RTC` class comes from `machine`:

```python
from machine import RTC
```

The time is stored as an **8-item tuple**:

```text
(year, month, day, weekday, hours, minutes, seconds, subseconds)
```

Note the **weekday** sits at index 3, which is why the hour is at index 4.

## `rtcInit` — create the clock

Creates an `RTC` object.

**Inputs / parameters**

- **var_name** — variable name (default `rtc`).

**Generated MicroPython**

```python
rtc = RTC()
```

## `rtcSetTime` — set the date and time

Sets the full date/time tuple.

**Inputs / parameters**

- **rtc_name** — the RTC variable (default `rtc`).
- **year, month, day** — defaults `2025`, `1`, `1`.
- **weekday** — `0`–`6` (default `0`).
- **hour, minute, second, subsecond** — defaults all `0`.

**Generated MicroPython**

```python
rtc.datetime((2025, 1, 1, 0, 0, 0, 0, 0))
```

## `rtcGetTime` — read the whole tuple

Reads the full date/time tuple at once.

**Inputs / parameters**

- **var_name** — variable for the result (default `current_time`).
- **rtc_name** — the RTC variable (default `rtc`).

**Generated MicroPython**

```python
current_time = rtc.datetime()
```

## Getting individual fields

Each of these is a **value block** — drop it where a number is expected. They
index into the tuple returned by `rtc.datetime()`.

| Block | Generated code | Returns |
|-------|----------------|---------|
| `rtcGetYear`   | `rtc.datetime()[0]` | year |
| `rtcGetMonth`  | `rtc.datetime()[1]` | month |
| `rtcGetDay`    | `rtc.datetime()[2]` | day |
| `rtcGetHour`   | `rtc.datetime()[4]` | hour |
| `rtcGetMinute` | `rtc.datetime()[5]` | minute |
| `rtcGetSecond` | `rtc.datetime()[6]` | second |

```python
print(rtc.datetime()[0], rtc.datetime()[1], rtc.datetime()[2])
```

## Wiring notes

- The internal RTC needs no wiring. For accurate time across power loss, add a
  battery-backed module (such as a DS3231) over I²C instead.

## Next

Continue to **[Watchdog »](wdt.md)**
