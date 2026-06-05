# Move & Turn

These three blocks are the heart of sprite motion: step forward along the
current heading, or rotate clockwise / counter-clockwise. They run in the
**simulator**, so you watch the sprite move on the stage.

## `spriteMoveSteps` — move N steps

Moves the selected sprite forward by a number of steps along whatever direction
it currently faces.

**Inputs**

- **sprite** — the sprite picker dropdown (default `cat`).
- **STEPS** — a Number value input (default shadow `10`).

**Generated code** (sprite `cat`, `STEPS = 10`):

```python
sprite.move_steps("cat", 10)
```

## `spriteTurnRight` — turn ↻ N degrees

Rotates the sprite **clockwise**.

**Inputs**

- **sprite** — sprite picker (default `cat`).
- **DEG** — a Number value input (default shadow `15`).

**Generated code** (sprite `cat`, `DEG = 15`):

```python
sprite.turn_right("cat", 15)
```

## `spriteTurnLeft` — turn ↺ N degrees

Rotates the sprite **counter-clockwise**.

**Inputs**

- **sprite** — sprite picker (default `cat`).
- **DEG** — a Number value input (default shadow `15`).

**Generated code** (sprite `cat`, `DEG = 15`):

```python
sprite.turn_left("cat", 15)
```

## Worked example: move and bounce

Move the cat forward, and if it hits the edge of the stage, bounce it back.
Place these in a loop so the sprite keeps travelling:

```python
sprite.move_steps("cat", 10)
sprite.if_on_edge_bounce("cat")
```

Each tick the cat steps 10 forward; when it reaches the edge,
`if_on_edge_bounce` flips its direction so it heads back across the stage.

## Next

Continue to **[Go to & glide »](goto-glide.md)**
