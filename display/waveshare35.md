# Waveshare 3.5" all-in-one display board

The **Waveshare 3.5"** board is an ESP32-S3 with a built-in colour TFT (driven by the
**AXS15231B** controller over **QSPI**) and a capacitive touch panel. Wiring up LVGL by
hand for this board takes dozens of lines — the **`waveshare35Init`** block does it all
in one drop.

> Requires **`lv_micropython`** firmware that includes `lcd_bus`, `axs15231b`,
> `lvgl`, `task_handler`, and the `fs_driver` helper.

## `waveshare35Init` — boot the whole display

This single block emits the complete startup sequence for the board. It imports the
needed modules, defines the board's pin constants, installs the AXS15231B QSPI
workarounds, allocates draw buffers, and creates the ready-to-use objects.

**Inputs:** none — the pins and timings are fixed for this board.

After it runs you have these objects available:

- `display` — the AXS15231B display driver
- `th` — a `task_handler.TaskHandler()` already running the LVGL loop
- `scrn` — the active screen (`lv.screen_active()`), with a dark background applied
- `fs_drv` — a filesystem driver registered on drive `"S"`

The generated code begins with the imports and constants, for example:

```python
import lcd_bus
import machine
from time import sleep
import axs15231b
import lvgl as lv
import task_handler
from fs_driver import fs_register

_WIDTH = 320
_HEIGHT = 480
_QSPI_D0 = 1
_QSPI_D1 = 2
_QSPI_D2 = 3
_QSPI_D3 = 4
_QSPI_CLK = 5
_LCD_CS = 12
_BL = 6
_LCD_FREQ = 40000000
```

…and ends by creating the display, task handler, screen, and filesystem driver:

```python
display = axs15231b.AXS15231B(...)
th = task_handler.TaskHandler()
scrn = lv.screen_active()
scrn.set_style_bg_color(lv.color_hex(0x101820), 0)
fs_drv = lv.fs_drv_t()
fs_register(fs_drv, "S")
```

(The full block is ~150 lines; the helper functions and pin setup in the middle are
generated for you and don't need editing.)

## Building a UI on top

Because `scrn` is the active screen and `th` already runs the LVGL loop, you can add
widgets straight after the init block — no manual `while True:` loop required:

```python
label1 = lv.label(scrn)
label1.set_text("Hello Waveshare")
label1.align(lv.ALIGN.CENTER, 0, 0)
```

## Next

Continue to [HTTP Requests](../../network/requests/index.md).
