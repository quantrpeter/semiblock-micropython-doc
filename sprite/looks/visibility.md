# Visibility & Costumes

These blocks decide whether a sprite is drawn on the **simulator** stage and
which **costume** (picture) it wears. A sprite can have several costumes;
switching between them is how you make simple frame-by-frame animation.

## `spriteShow` — show

Makes the selected sprite visible. Takes only the sprite picker (default `cat`).

**Generated code** (sprite `cat`):

```python
sprite.show("cat")
```

## `spriteHide` — hide

Hides the selected sprite. It still exists and keeps its position — it just
isn't drawn. Takes only the sprite picker.

**Generated code** (sprite `cat`):

```python
sprite.hide("cat")
```

## `spriteSwitchCostume` — switch costume to

Changes the sprite to a named costume. The **COSTUME** dropdown lists the
costumes belonging to whichever sprite is selected; if none are defined it falls
back to `costume1`.

**Inputs**

- **sprite** — sprite picker (default `cat`).
- **COSTUME** — costume dropdown (default `costume1`).

**Generated code** (sprite `cat`, costume `costume1`):

```python
sprite.switch_costume("cat", "costume1")
```

## Worked example: blink and swap

Hide the cat briefly, then show it again wearing a different costume:

```python
sprite.hide("cat")
await time.sleep(0.5)
sprite.switch_costume("cat", "costume2")
sprite.show("cat")
```

In the simulator, `time.sleep` is awaited so the half-second pause animates
correctly instead of freezing the stage.

## Next

Continue to **[Size »](size.md)**
