# Tutorial 1: The Dancing Penguin

## Overview
In this project, you will create an animated, dancing penguin! You will draw custom costumes, program code loops, control sprite movements, and play background music.

You will learn how to:
1. Choose and rename a sprite.
2. Draw two costumes for jumping animation.
3. Switch costumes inside a loop.
4. Move a sprite up and down using coordinates.
5. Play sound and music in the background.


## What You Are Building
* **Penguin Sprite:** Switches costumes and moves up and down to look like it is jumping and dancing.
* **Music:** Plays a fun sound effect in the background while the penguin jumps.


## Part 1 - Setup

> Before we begin coding our dancing penguin, let's set up our workspace by adding our main character and choosing a clean backdrop.


### Step 1 - Open the Designer Panel
Click **"Designer"** on the right panel to open the sprite and background controls.

> ![](img/Step1.png){width=inherit}


### Step 2 - Add a New Object
Click **"Add object"** as shown in the interface to open the object library.

> ![](img/Step2.png){width=inherit}

### Step 3 - Choose and Name Your Character
1. Search or scroll to find the **Penguin**.
2. Click to select it.
3. Change its name to **`Pen`**.

> ![](img/Step3.png){width=inherit}

### Step 4 - Select Stage Background"
The default background is a bit messy, so let's change it! Click the stage photo icon as shown in the interface.

> ![](img/Step4.png){width=inherit}

### Step 5 - Pick a Better Backdrop
Browse the backdrop gallery and select a clean, suitable background for **Pen** to dance on!

> ![](img/Step5.png){width=inherit}


## Part 2 - Core Building Blocks

> Now that Pen is on stage, let's learn the four basic skills needed to bring our penguin to life: drawing a costume, switching looks, moving around, and playing audio.

### Step 1 - Draw New Costumes
1. Click **Character**"** in the top-left corner of the panel.

> ![](img/Step6.png){width=inherit}

1. Click the **paint brush** button in the bottom-left corner to create a new costume.

> ![](img/Step7.png){width=inherit}

3. Use the tools to draw 2 more costumes. See the examples below:

> ![](img/costume.png){width=inherit}


### Part 3 - Switch Costumes
There are 2 ways to change costumes in microPython:
1. `switch costume to "costume1"` – Changes to a specific costume by name.

> ![](img/switch_costume.png){width=inherit}

2. `next costume` – Switches to the very next costume in your list.

> ![](img/next_costume.png){width=inherit}

Try both blocks by placing them inside a `when green flag clicked` block. After assembling your code, click **Run** in the right panel to test it!

> ![](img/test_costume.png){width=inherit} ![](img/.png){width=inherit}