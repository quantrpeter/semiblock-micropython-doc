# Looks

> ![](img/index1.png)

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

> ![](img/index2.png)

| Block | Generated code |
| ----- | -------------- |
| `spriteHide` | `sprite.hide("cat")` |

> ![](img/index3.png)

| Block | Generated code |
| ----- | -------------- |
| `spriteSwitchCostume` | `sprite.switch_costume("cat", "costume1")` |

> ![](img/index4.png)

| Block | Generated code |
| ----- | -------------- |
| `spriteSetSize` | `sprite.set_size("cat", 100)` |

> ![](img/index5.png)

| Block | Generated code |
| ----- | -------------- |
| `spriteGetSize` | `sprite.get_size("cat")` |

> ![](img/index6.png)

## Next

Continue to **[Visibility & costumes »](visibility.md)**
