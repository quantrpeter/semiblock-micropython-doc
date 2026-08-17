# How to Add & Play Sounds

Learn how to browse the sound library, upload custom audio, and trigger sound effects using MicroPython!

---

## Step 1 - Add & Customise Sounds
By default, every project comes with standard sound effects. If you want to add background music or unique effects, click **"Customise Sound"** in the panel to browse the sound library or upload your own audio files.

---

## Step 2 - Play Sounds with MicroPython

There are 2 main ways to play a sound in SemiBlock:

1. **`start_sound("pop")`** – Plays the sound immediately in the background while your code continues executing the next block without stopping.

> ![](img/start_sound.png){width=inherit}

1. **`play_sound_until_done("pop")`** – Plays the entire sound effect and pauses your script until the audio finishes playing.

> ![](img/play_sound.png){width=inherit}

---

> 💡 **Tip:** Use `start_sound()` for quick action effects (like jumping or clicking) and `play_sound_until_done()` when you want actions to sync with music!