# Go to & Glide

These blocks place the sprite at a spot on the stage. **Go to** jumps there
instantly; **glide** slides there smoothly over a number of seconds. Both run
in the **simulator**.

## Targets menu

`spriteGoToMenu`, `spriteGlideToMenu`, and the pointing blocks share a target
dropdown with these options:

| You pick | Generated argument |
| -------- | ------------------ |
| random position | `"_random_"` |
| mouse-pointer | `"_mouse_"` |
| *another sprite name* | `"that_sprite"` |

## `spriteGoToMenu` — go to a target

Instantly moves the sprite to a target location.

**Inputs:** sprite picker (default `cat`); **TO** dropdown (target).

**Generated code** (sprite `cat`, target *random position*):

```python
sprite.go_to("cat", "_random_")
```

## `spriteGoToXY` — go to x, y

Instantly moves the sprite to an exact stage coordinate.

**Inputs:** sprite picker; **X** and **Y** Number inputs (default shadows `0`).

**Generated code** (sprite `cat`, `X = 0`, `Y = 0`):

```python
sprite.goto("cat", 0, 0)
```

## `spriteGlideToMenu` — glide to a target

Smoothly slides the sprite to a target over **SECS** seconds. The simulator
animates the glide, so the generated call is **awaited**.

**Inputs:** sprite picker; **SECS** Number input (default shadow `1`); **TO**
target dropdown.

**Generated code** (sprite `cat`, `SECS = 1`, target *mouse-pointer*):

```python
await sprite.glide_to("cat", 1, "_mouse_")
```

## `spriteGlideToXY` — glide to x, y

Smoothly slides the sprite to an exact coordinate over **SECS** seconds, also
awaited.

**Inputs:** sprite picker; **SECS**, **X**, **Y** Number inputs (default
shadows `1`, `0`, `0`).

**Generated code** (sprite `cat`, `SECS = 1`, `X = 0`, `Y = 0`):

```python
await sprite.glide_to_xy("cat", 1, 0, 0)
```

## Worked example: slide across, then snap back

```python
await sprite.glide_to_xy("cat", 2, 100, 0)
sprite.goto("cat", -100, 0)
```

The cat glides smoothly to the right side over 2 seconds, then jumps back to the
left instantly — ready to glide again.

## Next

Continue to **[Pointing »](point.md)**
