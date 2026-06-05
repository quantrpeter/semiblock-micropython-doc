# Animation & Sprite Blocks

Part VII covers SemiBlock MicroPython's **Scratch-style sprite blocks**. If you
have ever used Scratch, these will feel instantly familiar: you tell a sprite
(a little character on the stage) to move, turn, glide, show, hide, change
costume, or react when it is clicked.

## These blocks run in the simulator

Unlike the hardware blocks in Part III, sprite blocks **do not run on your
ESP32 board**. They run inside the **built-in SemiBlock simulator** — a small
animated stage drawn in your browser. When you press **Run**, the editor turns
your blocks into calls to a Python `sprite` module that the simulator provides,
and you watch the cat (or any sprite you add) move around on screen.

Because everything happens in the browser, you can experiment with motion and
animation without wiring up any hardware.

## How the generated code looks

Every sprite block carries its own **sprite picker** dropdown. The chosen
sprite name (default `cat`) is passed as the first argument to a `sprite.*`
call. For example, dragging *move 10 steps* with the `cat` sprite selected
generates:

```python
sprite.move_steps("cat", 10)
```

The `sprite` module is supplied by the simulator runtime, so you never have to
`import` it yourself for motion and looks blocks — the [Events](events/index.md)
hat block adds the import automatically when needed.

## The three categories

- **[Motion](motion/index.md)** — move, turn, glide, point, and set/read the
  sprite's position and direction.
- **[Looks](looks/index.md)** — show, hide, switch costume, and set/read the
  sprite's size.
- **[Events](events/index.md)** — run blocks *when a sprite is clicked*.

## Next

Continue to **[Motion blocks »](motion/index.md)**
