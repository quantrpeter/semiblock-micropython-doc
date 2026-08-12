# Tutorial 1-3: Telling Jokes with MicroPython

![](img/Tut1-3/tut3_video.gif){width=inherit}

## Overview
In this project, you will create a dialogue animation between two characters on stage! The Bird will perform a jump, and then the Owl will perform a rolling motion across the screen.

You will learn how to:
1. Add and set up multiple characters on stage (`Bird` and `Owl`).
2. Use the `say` block for speech bubbles and timing dialogue.
3. Perform jump movements using Y-axis coordinates and costume changes.
4. Program rotation using `turn degrees` inside a `for` loop to create a roll animation.


## What You Are Building
* **Bird Sprite:** Says dialogue, jumps up (+25 Y), changes costumes, and lands back down (-25 Y).
* **Owl Sprite:** Speaks after the bird, then rotates 60 degrees and moves right (+10 X) inside a loop to roll across the screen.


## Part 1 - Setup
Before we begin coding our dialogue, let's set up our workspace by adding our two characters and choosing a suitable backdrop.


### Step 1 - Open the Designer Panel
Click **"Designer"** on the right panel to open the sprite and background controls.

> ![](img/Tut1-3/Step1.png){width=inherit}


### Step 2 - Add the First Character (`Bird`)

> ![](img/Tut1-3/Step2.png){width=inherit} ![](img/Tut1-3/Step3.png){width=inherit}

1. Click **"Add object"** to open the object library.
2. Search or scroll to find the **Bird**.
3. Select it and change its name to **`Bird`**.


### Step 3 - Add the Second Character (`Owl`)
1. Click **"Add object"** again.
2. Search or scroll to find the **Owl**.
3. Select it and change its name to **`Owl`**.


### Step 4 - Select Stage Background
Click the stage photo icon in the interface and choose a clear backdrop for **Bird** and **Owl**.

> ![](img/Tut1-3/Step4.png){width=inherit} ![](img/Tut1-3/Step5.png){width=inherit}


### Step 5 - Position the Characters Side by Side
Drag **Bird** to the left side of the stage and **Owl** to the right side so they are standing next to each other before the animation starts.

> ![](img/Tut1-3/Step6.png){width=inherit}


### Step 6 - Draw a Jumping Costume for Bird
1. Click **"Character"** in the top-left corner and select **`Bird`**.
2. Click the **paint brush** icon at the bottom-left to add a new costume.
3. Draw a jumping pose for **Bird** (e.g., wings spread upward or legs tucked).

> ![](img/Tut1-3/Step7.png){width=inherit} ![](img/Tut1-3/Step8.png){width=inherit}


## Part 2 - Core Building Blocks

Before combining everything, let's review the main blocks used in this project:

### Step 1 - Speech Bubbles (`say`)
Use `sprite.say_for_seconds(name, text, seconds)` to make characters speak in order. The script waits for the speech bubble time to finish before moving to the next block.

> ![](img/Tut1-3/say.png){width=inherit}


### Step 2 - Rotating Sprites (`turn`)
Use `turn right (degrees)` or `turn left (degrees)` to rotate your character. Combining rotation with movement inside a loop makes the sprite look like it is rolling!

> ![](img/Tut1-3/turn.png){width=inherit}


## Part 3 - Combine It All!

Here is the complete script to run the story sequence from start to finish:

### Complete Code

```python

# 1. Bird speaks and jumps
sprite.say_for_seconds("Bird", "Watch me! I am going to jump!", 2)
sprite.say_for_seconds("Bird", "3... 2... 1... Jump!", 2)

sprite.change_y("Bird", 25)
sprite.next_costume("Bird")
sleep(0.5)

sprite.change_y("Bird", -25)
sprite.next_costume("Bird")

# 2. Owl speaks and rolls
sprite.say_for_seconds("Owl", "Watch me! I am going to roll!", 2)

for x in range(12):
    sprite.turn_right("Owl", 60)
    sprite.change_x("Owl", 10)
    sleep(0.1)

```

> ![](img/Tut1-3/final_code.png){width=inherit}
