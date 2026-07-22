# Widgets — Container, Slider, Bar, Arc, Spinner

These widgets group content and show values. A **container** holds other widgets; a
**slider** lets the user pick a value; a **bar** and an **arc** display a value; a
**spinner** shows an indeterminate "loading" animation.

## `lvglContainerCreate` — container

A plain object used to group and lay out other widgets.

**Inputs:** container name, parent.

```python
container = lv.obj(scr)
```

> ![](img/ind1.png){width=inherit}

## `lvglSliderCreate` — slider

**Inputs:** slider name, parent.

```python
slider1 = lv.slider(scr)
```

> ![](img/ind2.png){width=inherit}

## `lvglSliderSetValue` — set slider value

**Inputs:** slider name, value, anim (animation on/off).

```python
slider1.set_value(50, lv.ANIM.OFF)
```

> ![](img/ind3.png){width=inherit}

## `lvglSliderGetValue` — read slider value

Stores the current slider value into a variable.

**Inputs:** var name, slider name.

```python
value = slider1.get_value()
```

> ![](img/ind4.png){width=inherit}

## `lvglBarCreate` — bar

A non-interactive progress bar.

**Inputs:** bar name, parent.

```python
bar1 = lv.bar(scr)
```

> ![](img/ind5.png){width=inherit}

## `lvglBarSetValue` — set bar value

**Inputs:** bar name, value, anim.

```python
bar1.set_value(70, lv.ANIM.OFF)
```

> ![](img/ind6.png){width=inherit}

## `lvglArcCreate` — arc

A circular indicator/dial.

**Inputs:** arc name, parent.

```python
arc1 = lv.arc(scr)
```

> ![](img/ind7.png){width=inherit}

## `lvglArcSetValue` — set arc value

**Inputs:** arc name, value.

```python
arc1.set_value(30)
```

> ![](img/ind8.png){width=inherit}

## `lvglSpinnerCreate` — spinner

A spinning "loading" indicator.

**Inputs:** spinner name, parent, speed, angle.

```python
spinner1 = lv.spinner(scr, 1000, 60)
```

> ![](img/ind9.png){width=inherit}

## Next

Continue to [Widgets — Checkbox, Switch, Textarea, Dropdown, Roller](widgets-input.md).
