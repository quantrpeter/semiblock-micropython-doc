# Looks

Looks blocks change how a sprite **appears** on the **simulator** stage: show
or hide it, switch its costume, and set or read its size. They are the purple
Scratch-style blocks.

Every Looks block carries a **sprite picker** dropdown (default `cat`) whose
value becomes the first argument of the generated `sprite.*` call. None of these
run on the microcontroller — they animate the browser stage.

## What's in this category

- **[Visibility & costumes](visibility.md)** — show, hide, and switch costume.
  - `spriteShow`, `spriteHide`, `spriteSwitchCostume`
- **[Size](size.md)** — set the sprite's scale and read it back.
  - `spriteSetSize`, `spriteGetSize`

## Quick reference

| Block | Generated code |
| ----- | -------------- |
| `spriteShow` | `sprite.show("cat")` |
| `spriteHide` | `sprite.hide("cat")` |
| `spriteSwitchCostume` | `sprite.switch_costume("cat", "costume1")` |
| `spriteSetSize` | `sprite.set_size("cat", 100)` |
| `spriteGetSize` | `sprite.get_size("cat")` |

## Next

Continue to **[Visibility & costumes »](visibility.md)**
