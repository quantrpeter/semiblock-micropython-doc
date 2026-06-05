# Position & Rotation

These blocks adjust the sprite's X / Y coordinates directly, bounce it off the
stage edges, and control how it looks while rotating. All run in the
**simulator**.

## `spriteChangeX` — change x by

Adds an amount to the sprite's current x-coordinate (moves it horizontally).

**Inputs:** sprite picker (default `cat`); **DX** Number input (default
shadow `10`).

**Generated code** (sprite `cat`, `DX = 10`):

```python
sprite.change_x("cat", 10)
```

## `spriteSetX` — set x to

Sets the sprite's x-coordinate to an exact value.

**Inputs:** sprite picker; **X** Number input (default shadow `0`).

**Generated code** (sprite `cat`, `X = 0`):

```python
sprite.set_x("cat", 0)
```

## `spriteChangeY` — change y by

Adds an amount to the sprite's current y-coordinate (moves it vertically).

**Inputs:** sprite picker; **DY** Number input (default shadow `10`).

**Generated code** (sprite `cat`, `DY = 10`):

```python
sprite.change_y("cat", 10)
```

## `spriteSetY` — set y to

Sets the sprite's y-coordinate to an exact value.

**Inputs:** sprite picker; **Y** Number input (default shadow `0`).

**Generated code** (sprite `cat`, `Y = 0`):

```python
sprite.set_y("cat", 0)
```

## `spriteIfOnEdgeBounce` — if on edge, bounce

If the sprite is touching the edge of the stage, flips its direction so it
heads back. Takes no value inputs — just the sprite picker.

**Generated code** (sprite `cat`):

```python
sprite.if_on_edge_bounce("cat")
```

## `spriteSetRotationStyle` — set rotation style

Controls how the sprite is drawn as it turns. The **STYLE** dropdown offers
`left-right`, `don't rotate`, and `all around` (the default).

**Generated code** (sprite `cat`, style *all around*):

```python
sprite.set_rotation_style("cat", "all around")
```

## Worked example: drift down and across

```python
sprite.change_x("cat", 10)
sprite.change_y("cat", -5)
sprite.if_on_edge_bounce("cat")
```

The cat slides 10 to the right and 5 down each tick, bouncing when it reaches a
wall.

## Next

Continue to **[Position getters »](getters.md)**
