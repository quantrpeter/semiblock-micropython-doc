# Project 1-4: Scene Switcher Menu

Learn how to create an interactive scene selector menu using button triggers to dynamically switch stage backdrops in MicroPython!

---

## 🎯 Learning Objectives
* **Event Triggers:** Detect clicks on specific button objects (`when Btn clicked`).
* **Stage Control:** Dynamically change backdrops using `switch_backdrop()`.
* **UI Design:** Set up clickable interface elements on stage.

---

## Step 1 - Add Button Objects & Backdrops
1. Add three button sprites to your stage from the Object Library and rename them to **`Btn1`**, **`Btn2`**, and **`Btn3`**.
2. Open the Backdrop Gallery and add three different backdrops: **`Blue Sky`**, **`Flower`**, and **`White`**.

> ![](projects/img/Tut1-4/Step1.png){width=inherit}

---

## Step 2 - Code the Button Events

Program each button to switch to its corresponding stage backdrop when clicked:

1. **Button 1:** Triggers the **`Blue Sky`** backdrop.
2. **Button 2:** Triggers the **`Flower`** backdrop.
3. **Button 3:** Triggers the **`White`** backdrop.

> ![](img/Tut1-4/code_blocks.png){width=inherit}

### MicroPython Code Equivalent

```python
# Button 1 Event
def when_Btn1_clicked():
    switch_backdrop("Blue Sky")

# Button 2 Event
def when_Btn2_clicked():
    switch_backdrop("Flower")

# Button 3 Event
def when_Btn3_clicked():
    switch_backdrop("White")