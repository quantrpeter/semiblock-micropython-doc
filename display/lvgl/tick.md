# Tick: `lvglTickInc`

LVGL keeps its own sense of time, which it uses for animations and timeouts. It needs to
be told how many milliseconds have passed — that is what the **tick** does.

## `lvglTickInc` — advance the LVGL tick

Tells LVGL that a number of milliseconds have elapsed since the last call. Call it
regularly (for example from a timer interrupt or your main loop) so animations run at
the right speed.

**Inputs:** ms (milliseconds elapsed).

```python
lv.tick_inc(5)
```

## Where it fits

A bare-bones loop that both advances the tick and processes LVGL work:

```python
import lvgl as lv
from time import sleep_ms
scr = lv.obj()
lv.scr_load(scr)
label1 = lv.label(scr)
label1.set_text("Ticking")
while True:
    lv.tick_inc(5)
    lv.task_handler()
    sleep_ms(5)
```

> If you use a `TaskHandler` (see [Task handler, FS driver, scrollbar mode](task-fs.md))
> or an all-in-one board block, the tick is often handled for you. Use `lvglTickInc`
> when you drive the LVGL loop yourself.

## Next

Continue to [Waveshare 3.5" all-in-one display board](../waveshare35.md).
