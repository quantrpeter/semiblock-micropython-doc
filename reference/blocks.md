# Full block reference (alphabetical)

Every block `type` available in the SemiBlock MicroPython toolbox, grouped by
category in the order the categories appear in `src/toolbox.js`. Within each
category the blocks are listed in toolbox order. Each entry has a one-line
description of what the block does.

## Machine

> ![](hardblock/hardblock_Machine.png){width=inherit}

| Image | Block `type` | Generated MicroPython |
| --- | --- | --- |
| ![](all_blocks/createMainMethod.png){width=inherit} | `createMainMethod` | The program entry point; wraps imports and the `### start` body. |
| ![](all_blocks/softReset.png){width=inherit} | `softReset` | `machine.soft_reset()` |
| ![](all_blocks/hardReset.png){width=inherit} | `hardReset` | `machine.reset()` |
| ![](all_blocks/sleep.png){width=inherit} | `sleep` | `time.sleep(1)` |
| ![](all_blocks/sleep_ms.png){width=inherit} | `sleep_ms` | `time.sleep_ms(1000)` |
| ![](all_blocks/sleep_us.png){width=inherit} | `sleep_us` | `time.sleep_us(1000)` |
| ![](all_blocks/connectWifi.png){width=inherit} | `connectWifi` | `connectWifi('SSID', 'PASSWORD')` |
| ![](all_blocks/mem8Read.png){width=inherit} | `mem8Read` | `machine.mem8[address]` |
| ![](all_blocks/mem16Read.png){width=inherit} | `mem16Read` | `machine.mem16[address]` |
| ![](all_blocks/mem32Read.png){width=inherit} | `mem32Read` | `machine.mem32[address]` |
| ![](all_blocks/mem8Write.png){width=inherit} | `mem8Write` | `machine.mem8[address] = value` |
| ![](all_blocks/mem16Write.png){width=inherit} | `mem16Write` | `machine.mem16[address] = value` |
| ![](all_blocks/mem32Write.png){width=inherit} | `mem32Write` | `machine.mem32[address] = value` |
| ![](all_blocks/getCPUFreq.png){width=inherit} | `getCPUFreq` | `machine.freq()` |
| ![](all_blocks/setCPUFreq.png){width=inherit} | `setCPUFreq` | `machine.freq(240000000)` |
| ![](all_blocks/ticksMs.png){width=inherit} | `ticksMs` | `time.ticks_ms()` |
| ![](all_blocks/ticksDiff.png){width=inherit} | `ticksDiff` | `time.ticks_diff(t1, t2)` |
| ![](all_blocks/bytearrayInit.png){width=inherit} | `bytearrayInit` | `bytearray(10)` |

## Motion (sprite)

> ![](hardblock/hardblock_Motion.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/spriteMoveSteps.png){width=inherit} | `spriteMoveSteps` | Move the sprite forward a number of steps. |
| ![](all_blocks/spriteTurnRight.png){width=inherit} | `spriteTurnRight` | Rotate the sprite clockwise. |
| ![](all_blocks/spriteTurnLeft.png){width=inherit} | `spriteTurnLeft` | Rotate the sprite anticlockwise. |
| ![](all_blocks/spriteGoToMenu.png){width=inherit} | `spriteGoToMenu` | Go to a target chosen from a menu. |
| ![](all_blocks/spriteGoToXY.png){width=inherit} | `spriteGoToXY` | Go to an absolute X/Y position. |
| ![](all_blocks/spriteGlideToMenu.png){width=inherit} | `spriteGlideToMenu` | Glide to a menu target over a number of seconds. |
| ![](all_blocks/spriteGlideToXY.png){width=inherit} | `spriteGlideToXY` | Glide to an X/Y position over a number of seconds. |
| ![](all_blocks/spritePointInDirection.png){width=inherit} | `spritePointInDirection` | Point in a specific direction (degrees). |
| ![](all_blocks/spritePointTowards.png){width=inherit} | `spritePointTowards` | Point towards a target. |
| ![](all_blocks/spriteChangeX.png){width=inherit} | `spriteChangeX` | Change the sprite's X by an amount. |
| ![](all_blocks/spriteSetX.png){width=inherit} | `spriteSetX` | Set the sprite's X position. |
| ![](all_blocks/spriteChangeY.png){width=inherit} | `spriteChangeY` | Change the sprite's Y by an amount. |
| ![](all_blocks/spriteSetY.png){width=inherit} | `spriteSetY` | Set the sprite's Y position. |
| ![](all_blocks/spriteIfOnEdgeBounce.png){width=inherit} | `spriteIfOnEdgeBounce` | Bounce when touching the stage edge. |
| ![](all_blocks/spriteSetRotationStyle.png){width=inherit} | `spriteSetRotationStyle` | Set the rotation style. |
| ![](all_blocks/spriteGetX.png){width=inherit} | `spriteGetX` | Report the sprite's X position. |
| ![](all_blocks/spriteGetY.png){width=inherit} | `spriteGetY` | Report the sprite's Y position. |
| ![](all_blocks/spriteGetDirection.png){width=inherit} | `spriteGetDirection` | Report the sprite's direction. |

## Looks (sprite)

> ![](hardblock/hardblock_Looks.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/spriteShow.png){width=inherit} | `spriteShow` | Show the sprite. |
| ![](all_blocks/spriteHide.png){width=inherit} | `spriteHide` | Hide the sprite. |
| ![](all_blocks/spriteSwitchCostume.png){width=inherit} | `spriteSwitchCostume` | Switch to another costume. |
| ![](all_blocks/spriteSetSize.png){width=inherit} | `spriteSetSize` | Set the sprite size (percent). |
| ![](all_blocks/spriteGetSize.png){width=inherit} | `spriteGetSize` | Report the sprite size. |

## Events (sprite)

> ![](hardblock/hardblock_Events.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/spriteWhenClicked.png){width=inherit} | `spriteWhenClicked` | Run blocks when the sprite is clicked. |

## Waveshare 3.5

> ![](hardblock/hardblock_Waveshare.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/waveshare35Init.png){width=inherit} | `waveshare35Init` | Initialise the Waveshare 3.5" all-in-one display board. |

## Language

> ![](hardblock/hardblock_Language.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/freeCode.png){width=inherit} | `freeCode` | Insert a raw line of MicroPython. |
| ![](all_blocks/importCode.png){width=inherit} | `importCode` | `import <library>`. |
| ![](all_blocks/importCode2.png){width=inherit} | `importCode2` | `import <library> as <alias>`. |
| ![](all_blocks/fromImportCode.png){width=inherit} | `fromImportCode` | `from <library> import <component>`. |
| ![](all_blocks/forLoop.png){width=inherit} | `forLoop` | `for` loop over a range. |
| ![](all_blocks/whileLoop.png){width=inherit} | `whileLoop` | `while` loop. |
| ![](all_blocks/ifLoop.png){width=inherit} | `ifLoop` | `if` statement. |
| ![](all_blocks/elseIfLoop.png){width=inherit} | `elseIfLoop` | `elif` branch. |
| ![](all_blocks/elseLoop.png){width=inherit} | `elseLoop` | `else` branch. |
| ![](all_blocks/print.png){width=inherit} | `print` | Print a value to the REPL. |
| ![](all_blocks/variable.png){width=inherit} | `variable` | Assign a value to a variable. |
| ![](all_blocks/comment.png){width=inherit} | `comment` | A `#` comment line. |
| ![](all_blocks/pass.png){width=inherit} | `pass` | The `pass` statement. |
| ![](all_blocks/def.png){width=inherit} | `def` | Define a function. |
| ![](all_blocks/startThread.png){width=inherit} | `startThread` | Start a new thread with `_thread`. |

## List

> ![](hardblock/hardblock_List.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/createList.png){width=inherit} | `createList` | Create a list literal. |
| ![](all_blocks/appendList.png){width=inherit} | `appendList` | Append a value. |
| ![](all_blocks/insertList.png){width=inherit} | `insertList` | Insert a value at an index. |
| ![](all_blocks/removeList.png){width=inherit} | `removeList` | Remove a value. |
| ![](all_blocks/popList.png){width=inherit} | `popList` | Pop an item at an index. |
| ![](all_blocks/sortList.png){width=inherit} | `sortList` | Sort the list in place. |
| ![](all_blocks/reverseList.png){width=inherit} | `reverseList` | Reverse the list in place. |
| ![](all_blocks/lenList.png){width=inherit} | `lenList` | Length of the list. |
| ![](all_blocks/getList.png){width=inherit} | `getList` | Get the item at an index. |
| ![](all_blocks/getListSlice.png){width=inherit} | `getListSlice` | Slice `[start:end]`. |
| ![](all_blocks/getListSlice2.png){width=inherit} | `getListSlice2` | Slice `[start:]`. |
| ![](all_blocks/getListSlice3.png){width=inherit} | `getListSlice3` | Slice `[:end]`. |
| ![](all_blocks/getListSlice4.png){width=inherit} | `getListSlice4` | Copy slice `[:]`. |

## Dictionary

> ![](hardblock/hardblock_Dict.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/createDict.png){width=inherit} | `createDict` | Create an empty dict. |
| ![](all_blocks/dictSet.png){width=inherit} | `dictSet` | Set `dict[key] = value`. |
| ![](all_blocks/dictGet.png){width=inherit} | `dictGet` | Get `dict[key]`. |
| ![](all_blocks/dictKeys.png){width=inherit} | `dictKeys` | Get `dict.keys()`. |
| ![](all_blocks/dictValues.png){width=inherit} | `dictValues` | Get `dict.values()`. |
| ![](all_blocks/dictItems.png){width=inherit} | `dictItems` | Get `dict.items()`. |
| ![](all_blocks/dictPop.png){width=inherit} | `dictPop` | Pop a key. |
| ![](all_blocks/dictUpdate.png){width=inherit} | `dictUpdate` | Update from another dict. |
| ![](all_blocks/dictClear.png){width=inherit} | `dictClear` | Clear the dict. |

## Math

> ![](hardblock/hardblock_Math.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/integerInit.png){width=inherit} | `integerInit` | An integer literal. |
| ![](all_blocks/mathAdd.png){width=inherit} | `mathAdd` | Addition. |
| ![](all_blocks/mathSubtract.png){width=inherit} | `mathSubtract` | Subtraction. |
| ![](all_blocks/mathMultiply.png){width=inherit} | `mathMultiply` | Multiplication. |
| ![](all_blocks/mathDivide.png){width=inherit} | `mathDivide` | Division. |
| ![](all_blocks/mathModulo.png){width=inherit} | `mathModulo` | Modulo. |
| ![](all_blocks/mathPower.png){width=inherit} | `mathPower` | Exponentiation. |
| ![](all_blocks/mathSqrt.png){width=inherit} | `mathSqrt` | Square root. |
| ![](all_blocks/mathSin.png){width=inherit} | `mathSin` | Sine. |
| ![](all_blocks/mathCos.png){width=inherit} | `mathCos` | Cosine. |
| ![](all_blocks/mathTan.png){width=inherit} | `mathTan` | Tangent. |
| ![](all_blocks/mathLog.png){width=inherit} | `mathLog` | Logarithm. |
| ![](all_blocks/mathExp.png){width=inherit} | `mathExp` | Exponential. |
| ![](all_blocks/mathAbs.png){width=inherit} | `mathAbs` | Absolute value. |
| ![](all_blocks/mathFloor.png){width=inherit} | `mathFloor` | Floor. |
| ![](all_blocks/mathCeil.png){width=inherit} | `mathCeil` | Ceiling. |
| ![](all_blocks/mathRound.png){width=inherit} | `mathRound` | Round. |
| ![](all_blocks/mathMin.png){width=inherit} | `mathMin` | Minimum. |
| ![](all_blocks/mathMax.png){width=inherit} | `mathMax` | Maximum. |
| ![](all_blocks/mathPi.png){width=inherit} | `mathPi` | The constant π. |
| ![](all_blocks/mathE.png){width=inherit} | `mathE` | The constant e. |
| ![](all_blocks/mathRandom.png){width=inherit} | `mathRandom` | Random float. |
| ![](all_blocks/mathRandomInt.png){width=inherit} | `mathRandomInt` | Random integer. |
| ![](all_blocks/divmod.png){width=inherit} | `divmod` | `divmod()` quotient and remainder. |
| ![](all_blocks/hex.png){width=inherit} | `hex` | Hexadecimal string. |
| ![](all_blocks/ord.png){width=inherit} | `ord` | Unicode code point. |

## String

> ![](hardblock/hardblock_String.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/stringInit.png){width=inherit} | `stringInit` | A string literal. |
| ![](all_blocks/stringUpper.png){width=inherit} | `stringUpper` | Upper-case. |
| ![](all_blocks/stringLower.png){width=inherit} | `stringLower` | Lower-case. |
| ![](all_blocks/stringStrip.png){width=inherit} | `stringStrip` | Strip whitespace. |
| ![](all_blocks/stringReplace.png){width=inherit} | `stringReplace` | Replace substring. |
| ![](all_blocks/stringFind.png){width=inherit} | `stringFind` | Find substring index. |
| ![](all_blocks/stringSplit.png){width=inherit} | `stringSplit` | Split on a delimiter. |
| ![](all_blocks/stringJoin.png){width=inherit} | `stringJoin` | Join a list with a delimiter. |
| ![](all_blocks/stringStartsWith.png){width=inherit} | `stringStartsWith` | Prefix test. |
| ![](all_blocks/stringEndsWith.png){width=inherit} | `stringEndsWith` | Suffix test. |
| ![](all_blocks/stringLength.png){width=inherit} | `stringLength` | String length. |

## Random

> ![](hardblock/hardblock_Random.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/random.png){width=inherit} | `random` | Random float in `[0, 1)`. |
| ![](all_blocks/randint.png){width=inherit} | `randint` | Random integer in a range. |
| ![](all_blocks/choice.png){width=inherit} | `choice` | Random element from a sequence. |
| ![](all_blocks/shuffle.png){width=inherit} | `shuffle` | Shuffle a sequence in place. |
| ![](all_blocks/uniform.png){width=inherit} | `uniform` | Random float in a range. |
| ![](all_blocks/randrange.png){width=inherit} | `randrange` | Random value from a range with a step. |
| ![](all_blocks/sample.png){width=inherit} | `sample` | Random sample of unique elements. |

## Exception

> ![](hardblock/hardblock_Exception.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/tryExcept.png){width=inherit} | `tryExcept` | `try` / `except` block. |
| ![](all_blocks/raiseException.png){width=inherit} | `raiseException` | `raise` an exception. |
| ![](all_blocks/assertStatement.png){width=inherit} | `assertStatement` | `assert` a condition. |
| ![](all_blocks/finallyBlock.png){width=inherit} | `finallyBlock` | `finally` clause. |

## Regex

> ![](hardblock/hardblock_Regex.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/reMatch.png){width=inherit} | `reMatch` | `re.match`. |
| ![](all_blocks/reSearch.png){width=inherit} | `reSearch` | `re.search`. |
| ![](all_blocks/reFindAll.png){width=inherit} | `reFindAll` | `re.findall`. |
| ![](all_blocks/reFindIter.png){width=inherit} | `reFindIter` | `re.finditer`. |
| ![](all_blocks/reSub.png){width=inherit} | `reSub` | `re.sub`. |
| ![](all_blocks/reSplit.png){width=inherit} | `reSplit` | `re.split`. |
| ![](all_blocks/reCompile.png){width=inherit} | `reCompile` | `re.compile`. |

## Requests

> ![](hardblock/hardblock_Req.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/urequestsGet.png){width=inherit} | `urequestsGet` | HTTP `GET`. |
| ![](all_blocks/urequestsPost.png){width=inherit} | `urequestsPost` | HTTP `POST` with data. |
| ![](all_blocks/urequestsPut.png){width=inherit} | `urequestsPut` | HTTP `PUT` with data. |
| ![](all_blocks/urequestsDelete.png){width=inherit} | `urequestsDelete` | HTTP `DELETE`. |
| ![](all_blocks/urequestsHead.png){width=inherit} | `urequestsHead` | HTTP `HEAD`. |

## SemiBlock IoT

> ![](hardblock/hardblock_IoT.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/iotConnect.png){width=inherit} | `iotConnect` | Set the IoT server, device ID, and secret. |
| ![](all_blocks/iotPushReading.png){width=inherit} | `iotPushReading` | Push a single sensor reading to the cloud. |
| ![](all_blocks/iotPushValue.png){width=inherit} | `iotPushValue` | Push a keyed value to the cloud. |

## CSV

> ![](hardblock/hardblock_CSV.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/csvRead.png){width=inherit} | `csvRead` | Read all rows of a CSV file into a list. |
| ![](all_blocks/csvWrite.png){width=inherit} | `csvWrite` | Write rows to a CSV file. |
| ![](all_blocks/csvAppend.png){width=inherit} | `csvAppend` | Append a row to a CSV file. |

## OS

> ![](hardblock/hardblock_OS.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/osListDir.png){width=inherit} | `osListDir` | List directory contents. |
| ![](all_blocks/osRemove.png){width=inherit} | `osRemove` | Remove a file. |
| ![](all_blocks/osRename.png){width=inherit} | `osRename` | Rename a file. |
| ![](all_blocks/osMkdir.png){width=inherit} | `osMkdir` | Make a directory. |
| ![](all_blocks/osRmdir.png){width=inherit} | `osRmdir` | Remove a directory. |
| ![](all_blocks/osGetcwd.png){width=inherit} | `osGetcwd` | Current working directory. |
| ![](all_blocks/osChdir.png){width=inherit} | `osChdir` | Change directory. |
| ![](all_blocks/osStat.png){width=inherit} | `osStat` | File status. |
| ![](all_blocks/osUname.png){width=inherit} | `osUname` | System information. |
| ![](all_blocks/osSync.png){width=inherit} | `osSync` | Flush filesystem buffers. |
| ![](all_blocks/osSystem.png){width=inherit} | `osSystem` | Run a system command. |
| ![](all_blocks/osUrandom.png){width=inherit} | `osUrandom` | Random bytes. |

## Display (SSD1306)

> ![](hardblock/hardblock_Display.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/ssd1306.png){width=inherit} | `ssd1306` | Create an SSD1306 I²C display object. |
| ![](all_blocks/ssd1306_fill.png){width=inherit} | `ssd1306_fill` | Fill the screen buffer. |
| ![](all_blocks/ssd1306_show.png){width=inherit} | `ssd1306_show` | Flush the buffer to the screen. |
| ![](all_blocks/ssd1306_contrast.png){width=inherit} | `ssd1306_contrast` | Set contrast. |
| ![](all_blocks/ssd1306_invert.png){width=inherit} | `ssd1306_invert` | Invert colours. |
| ![](all_blocks/ssd1306_rotate.png){width=inherit} | `ssd1306_rotate` | Rotate the display. |
| ![](all_blocks/ssd1306_text.png){width=inherit} | `ssd1306_text` | Draw text. |
| ![](all_blocks/ssd1306_pixel.png){width=inherit} | `ssd1306_pixel` | Set a pixel. |
| ![](all_blocks/ssd1306_hline.png){width=inherit} | `ssd1306_hline` | Horizontal line. |
| ![](all_blocks/ssd1306_vline.png){width=inherit} | `ssd1306_vline` | Vertical line. |
| ![](all_blocks/ssd1306_line.png){width=inherit} | `ssd1306_line` | Arbitrary line. |
| ![](all_blocks/ssd1306_rect.png){width=inherit} | `ssd1306_rect` | Rectangle outline. |
| ![](all_blocks/ssd1306_fillRect.png){width=inherit} | `ssd1306_fillRect` | Filled rectangle. |
| ![](all_blocks/ssd1306_circle.png){width=inherit} | `ssd1306_circle` | Circle outline. |
| ![](all_blocks/ssd1306_fillCircle.png){width=inherit} | `ssd1306_fillCircle` | Filled circle. |
| ![](all_blocks/ssd1306_scroll.png){width=inherit} | `ssd1306_scroll` | Scroll the buffer. |
| ![](all_blocks/imageEditor.png){width=inherit} | `imageEditor` | Draw a bitmap in the SemiBlock image editor. |
| ![](all_blocks/drawPixels.png){width=inherit} | `drawPixels` | Render an edited bitmap to the display. |
| ![](all_blocks/ssd1306_setColor.png){width=inherit} | `ssd1306_setColor` | Set the draw colour. |
| ![](all_blocks/ssd1306_setFontSize.png){width=inherit} | `ssd1306_setFontSize` | Set the font size. |

## LVGL

| Block `type` | Description |
| --- | --- |
| `lvglInit` | `import lvgl as lv`. |
| `importLcdBus` | Import the LCD bus module. |
| `importSt7796` | Import the ST7796 driver. |
| `importSt7735` | Import the ST7735 driver. |
| `importTaskHandler` | Import the task handler. |
| `importFsDriver` | Import the filesystem driver. |
| `lcdSpiBusInit` | Initialise the LCD SPI bus. |
| `allocateFramebuffer` | Allocate a framebuffer. |
| `st7796Init` | Initialise an ST7796 panel. |
| `st7735Init` | Initialise an ST7735 panel. |
| `displayInit` | Generic display init. |
| `displayInitWithType` | Display init with a panel type. |
| `displaySetRotation` | Set screen rotation. |
| `displaySetColorInversion` | Toggle colour inversion. |
| `displaySetBacklight` | Set backlight level. |
| `taskHandlerInit` | Initialise the LVGL task handler. |
| `lvglFsDrvtInit` | Initialise the LVGL FS driver. |
| `lvglFsRegister` | Register the FS driver. |
| `lvglSetScrollbarMode` | Set scrollbar mode. |
| `lvglScreenCreate` | Create a screen object. |
| `lvglScreenLoad` | Load a screen. |
| `lvglScreenActive` | Get the active screen. |
| `lvglRefrNow` | Force an immediate refresh. |
| `lvglTaskHandler` | Run one task-handler pass. |
| `lvglLabelCreate` | Create a label. |
| `lvglLabelSetText` | Set label text. |
| `lvglButtonCreate` | Create a button. |
| `lvglContainerCreate` | Create a container. |
| `lvglSetPos` | Set object position. |
| `lvglSetSize` | Set object size. |
| `lvglSetWidth` | Set object width. |
| `lvglSetHeight` | Set object height. |
| `lvglSetX` | Set object X. |
| `lvglSetY` | Set object Y. |
| `lvglAlign` | Align an object. |
| `lvglSliderCreate` | Create a slider. |
| `lvglSliderSetValue` | Set slider value. |
| `lvglSliderGetValue` | Get slider value. |
| `lvglBarCreate` | Create a bar. |
| `lvglBarSetValue` | Set bar value. |
| `lvglArcCreate` | Create an arc. |
| `lvglArcSetValue` | Set arc value. |
| `lvglCheckboxCreate` | Create a checkbox. |
| `lvglCheckboxSetText` | Set checkbox text. |
| `lvglSwitchCreate` | Create a switch. |
| `lvglTextareaCreate` | Create a text area. |
| `lvglTextareaSetText` | Set text-area text. |
| `lvglDropdownCreate` | Create a dropdown. |
| `lvglDropdownSetOptions` | Set dropdown options. |
| `lvglRollerCreate` | Create a roller. |
| `lvglRollerSetOptions` | Set roller options. |
| `lvglImageCreate` | Create an image. |
| `lvglImageSetSrc` | Set image source. |
| `lvglImageSetSrcCostume` | Set image source from a costume. |
| `lvglLedCreate` | Create an LED widget. |
| `lvglLedOn` | Turn the LED widget on. |
| `lvglLedOff` | Turn the LED widget off. |
| `lvglLedToggle` | Toggle the LED widget. |
| `lvglLedSetBrightness` | Set LED-widget brightness. |
| `lvglKeyboardCreate` | Create a keyboard. |
| `lvglKeyboardSetTextarea` | Bind keyboard to a text area. |
| `lvglTabviewCreate` | Create a tab view. |
| `lvglTabviewAddTab` | Add a tab. |
| `lvglSetBgColor` | Set background colour. |
| `lvglSetTextColor` | Set text colour. |
| `lvglSetOpacity` | Set opacity. |
| `lvglSetStyleTextFont` | Set the text font style. |
| `lvglSetStyleBgOpa` | Set the background-opacity style. |
| `lvglSetStyleRadius` | Set the corner-radius style. |
| `lvglSetStylePad` | Set the padding style. |
| `lvglSetStyleBorderWidth` | Set the border-width style. |
| `lvglSetStyleBorderColor` | Set the border-colour style. |
| `lvglSetStyleShadowWidth` | Set the shadow-width style. |
| `lvglSetStyleShadowColor` | Set the shadow-colour style. |
| `lvglColorHex` | Make a colour from a hex value. |
| `lvglGetDisplay` | Get the display handle. |
| `lvglAddEventCb` | Add an event callback. |
| `lvglSpinnerCreate` | Create a spinner. |
| `lvglChartCreate` | Create a chart. |
| `lvglChartAddSeries` | Add a chart series. |
| `lvglChartSetPoint` | Set a chart point. |
| `lvglMeterCreate` | Create a meter. |
| `lvglAddFlag` | Add an object flag. |
| `lvglClearFlag` | Clear an object flag. |
| `lvglRemoveFlag` | Remove an object flag. |
| `lvglAnimCreate` | Create an animation. |
| `lvglAnimInit` | Initialise an animation. |
| `lvglAnimSetVar` | Set the animation target. |
| `lvglAnimSetTime` | Set the animation duration. |
| `lvglAnimSetValues` | Set the animation start/end. |
| `lvglAnimStart` | Start an animation. |
| `lvglObjDelete` | Delete an object. |
| `lvglObjClean` | Remove an object's children. |
| `lvglObjInvalidate` | Mark an object for redraw. |
| `lvglCanvasCreate` | Create a canvas. |
| `lvglCanvasSetBuffer` | Set the canvas buffer. |
| `lvglCanvasFillBg` | Fill the canvas background. |
| `lvglCanvasSetPx` | Set a canvas pixel. |
| `lvglTickInc` | Advance the LVGL tick counter. |

## Pin

| Block `type` | Description |
| --- | --- |
| `pin` | Create a `Pin` with a direction. |
| `pin2` | Create a `Pin` with input + pull type. |
| `on` | Drive the pin high. |
| `off` | Drive the pin low. |
| `pinValue` | Read the pin value. |
| `uartInit` | Initialise a UART. |
| `uartRead` | Read bytes from UART. |
| `uartWrite` | Write to UART. |
| `neoPixel` | Create a NeoPixel strip. |
| `neoPixelWrite` | Set and write a NeoPixel colour. |

## Timer

| Block `type` | Description |
| --- | --- |
| `timerInit` | Create a `Timer`. |
| `timerStart` | Start a periodic/one-shot timer. |
| `timerStop` | De-initialise the timer. |

## PWM

| Block `type` | Description |
| --- | --- |
| `pwmInit` | Create a PWM on a pin. |
| `pwmSetFreq` | Set PWM frequency. |
| `pwmSetDuty` | Set PWM duty cycle. |
| `pwmDeinit` | De-initialise PWM. |

## ADC

| Block `type` | Description |
| --- | --- |
| `adcInit` | Create an ADC on a pin. |
| `adcRead` | Read the ADC. |
| `dacInit` | Create a DAC on a pin. |
| `dacWrite` | Write to the DAC. |

## SPI

| Block `type` | Description |
| --- | --- |
| `spiInit` | Create a hardware SPI. |
| `spiBusInit` | Initialise an SPI bus. |
| `spiRead` | Read from SPI. |
| `spiWrite` | Write to SPI. |
| `spiReadWrite` | Full-duplex read into a buffer. |

## I2C

| Block `type` | Description |
| --- | --- |
| `i2cInit` | Create an I²C bus. |
| `i2cScan` | Scan for I²C addresses. |
| `i2cRead` | Read from a device. |
| `i2cWrite` | Write to a device. |

## WatchDog (RTC, WDT, deep sleep)

| Block `type` | Description |
| --- | --- |
| `rtcInit` | Create an `RTC`. |
| `rtcSetTime` | Set the RTC datetime. |
| `rtcGetTime` | Get the RTC datetime tuple. |
| `rtcGetYear` | Get the year. |
| `rtcGetMonth` | Get the month. |
| `rtcGetDay` | Get the day. |
| `rtcGetHour` | Get the hour. |
| `rtcGetMinute` | Get the minute. |
| `rtcGetSecond` | Get the second. |
| `wdtInit` | Create a watchdog timer. |
| `wdtFeed` | Feed the watchdog. |
| `deepSleep` | Enter deep sleep for a duration. |

## SD Card

| Block `type` | Description |
| --- | --- |
| `sdCardInit` | Create an `SDCard`. |
| `sdCardMount` | Mount the card. |
| `sdCardUnmount` | Unmount the card. |
| `sdCardFileWrite` | Write a file to the card. |
| `sdCardFileRead` | Read a file from the card. |

## RMT

| Block `type` | Description |
| --- | --- |
| `rmtInit` | Create an RMT channel. |
| `rmtWrite` | Write RMT pulses. |
| `rmtDeinit` | De-initialise RMT. |

## One-Wire

| Block `type` | Description |
| --- | --- |
| `oneWireInit` | Create a OneWire bus. |
| `oneWireScan` | Scan for OneWire devices. |
| `oneWireRead` | Read a byte. |
| `oneWireWrite` | Write a byte. |

## Capacitive Touch

| Block `type` | Description |
| --- | --- |
| `touchInit` | Create a `TouchPad`. |
| `touchRead` | Read the touch value. |

## DHT

| Block `type` | Description |
| --- | --- |
| `dhtInit` | Create a DHT sensor. |
| `dhtReadTemperature` | Measure and read temperature. |
| `dhtReadHumidity` | Measure and read humidity. |

## HC-SR04 Sonar

| Block `type` | Description |
| --- | --- |
| `hcsr04Init` | Define the driver and create an HC-SR04 sensor. |
| `hcsr04DistanceCm` | Read distance in centimetres. |
| `hcsr04DistanceMm` | Read distance in millimetres. |

## Sensors

| Block `type` | Description |
| --- | --- |
| `temperature` | Read an analog thermistor via `getTemperature`. |
| `fourDigitDisplay` | Create a TM1637 4-digit display. |
| `fourDigitDisplay_setNumber` | Show a number on the display. |
| `motor` | Create a DC-motor control pin. |
| `motorOn` | Turn the motor on. |
| `motorOff` | Turn the motor off. |
| `servo` | Create a servo. |
| `servoAngle` | Set the servo angle. |

## Generative AI

| Block `type` | Description |
| --- | --- |
| `askDeepSeek` | Ask a DeepSeek LLM a question and store the answer. |

## Open Data

| Block `type` | Description |
| --- | --- |
| `getOpenDataTemperature` | Get temperature for a location. |
| `getOpenDataRainfall` | Get rainfall for a location. |
| `getOpenDataHumidity` | Get humidity. |
| `getPublicHoliday` | Get public holiday data. |
| `getBusStopID` | Look up a bus stop ID. |
| `getBusRouteNo` | Look up a bus route number. |
| `getBusArrivalTime` | Get bus arrival time. |
| `getFlightList` | Get a flight list. |
| `getMTR` | Get MTR information. |

---

**Next:** [Category color legend](categories.md)
