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

> ![](hardblock/hardblock_LVGL.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/lvglInit.png){width=inherit} | `lvglInit` | `import lvgl as lv`. |
| ![](all_blocks/importLcdBus.png){width=inherit} | `importLcdBus` | Import the LCD bus module. |
| ![](all_blocks/importSt7796.png){width=inherit} | `importSt7796` | Import the ST7796 driver. |
| ![](all_blocks/importSt7735.png){width=inherit} | `importSt7735` | Import the ST7735 driver. |
| ![](all_blocks/importTaskHandler.png){width=inherit} | `importTaskHandler` | Import the task handler. |
| ![](all_blocks/importFsDriver.png){width=inherit} | `importFsDriver` | Import the filesystem driver. |
| ![](all_blocks/lcdSpiBusInit.png){width=inherit} | `lcdSpiBusInit` | Initialise the LCD SPI bus. |
| ![](all_blocks/allocateFramebuffer.png){width=inherit} | `allocateFramebuffer` | Allocate a framebuffer. |
| ![](all_blocks/st7796Init.png){width=inherit} | `st7796Init` | Initialise an ST7796 panel. |
| ![](all_blocks/st7735Init.png){width=inherit} | `st7735Init` | Initialise an ST7735 panel. |
| ![](all_blocks/displayInit.png){width=inherit} | `displayInit` | Generic display init. |
| ![](all_blocks/displayInitWithType.png){width=inherit} | `displayInitWithType` | Display init with a panel type. |
| ![](all_blocks/displaySetRotation.png){width=inherit} | `displaySetRotation` | Set screen rotation. |
| ![](all_blocks/displaySetColorInversion.png){width=inherit} | `displaySetColorInversion` | Toggle colour inversion. |
| ![](all_blocks/displaySetBacklight.png){width=inherit} | `displaySetBacklight` | Set backlight level. |
| ![](all_blocks/taskHandlerInit.png){width=inherit} | `taskHandlerInit` | Initialise the LVGL task handler. |
| ![](all_blocks/lvglFsDrvtInit.png){width=inherit} | `lvglFsDrvtInit` | Initialise the LVGL FS driver. |
| ![](all_blocks/lvglFsRegister.png){width=inherit} | `lvglFsRegister` | Register the FS driver. |
| ![](all_blocks/lvglSetScrollbarMode.png){width=inherit} | `lvglSetScrollbarMode` | Set scrollbar mode. |
| ![](all_blocks/lvglScreenCreate.png){width=inherit} | `lvglScreenCreate` | Create a screen object. |
| ![](all_blocks/lvglScreenLoad.png){width=inherit} | `lvglScreenLoad` | Load a screen. |
| ![](all_blocks/lvglScreenActive.png){width=inherit} | `lvglScreenActive` | Get the active screen. |
| ![](all_blocks/lvglRefrNow.png){width=inherit} | `lvglRefrNow` | Force an immediate refresh. |
| ![](all_blocks/lvglTaskHandler.png){width=inherit} | `lvglTaskHandler` | Run one task-handler pass. |
| ![](all_blocks/lvglLabelCreate.png){width=inherit} | `lvglLabelCreate` | Create a label. |
| ![](all_blocks/lvglLabelSetText.png){width=inherit} | `lvglLabelSetText` | Set label text. |
| ![](all_blocks/lvglButtonCreate.png){width=inherit} | `lvglButtonCreate` | Create a button. |
| ![](all_blocks/lvglContainerCreate.png){width=inherit} | `lvglContainerCreate` | Create a container. |
| ![](all_blocks/lvglSetPos.png){width=inherit} | `lvglSetPos` | Set object position. |
| ![](all_blocks/lvglSetSize.png){width=inherit} | `lvglSetSize` | Set object size. |
| ![](all_blocks/lvglSetWidth.png){width=inherit} | `lvglSetWidth` | Set object width. |
| ![](all_blocks/lvglSetHeight.png){width=inherit} | `lvglSetHeight` | Set object height. |
| ![](all_blocks/lvglSetX.png){width=inherit} | `lvglSetX` | Set object X. |
| ![](all_blocks/lvglSetY.png){width=inherit} | `lvglSetY` | Set object Y. |
| ![](all_blocks/lvglAlign.png){width=inherit} | `lvglAlign` | Align an object. |
| ![](all_blocks/lvglSliderCreate.png){width=inherit} | `lvglSliderCreate` | Create a slider. |
| ![](all_blocks/lvglSliderSetValue.png){width=inherit} | `lvglSliderSetValue` | Set slider value. |
| ![](all_blocks/lvglSliderGetValue.png){width=inherit} | `lvglSliderGetValue` | Get slider value. |
| ![](all_blocks/lvglBarCreate.png){width=inherit} | `lvglBarCreate` | Create a bar. |
| ![](all_blocks/lvglBarSetValue.png){width=inherit} | `lvglBarSetValue` | Set bar value. |
| ![](all_blocks/lvglArcCreate.png){width=inherit} | `lvglArcCreate` | Create an arc. |
| ![](all_blocks/lvglArcSetValue.png){width=inherit} | `lvglArcSetValue` | Set arc value. |
| ![](all_blocks/lvglCheckboxCreate.png){width=inherit} | `lvglCheckboxCreate` | Create a checkbox. |
| ![](all_blocks/lvglCheckboxSetText.png){width=inherit} | `lvglCheckboxSetText` | Set checkbox text. |
| ![](all_blocks/lvglSwitchCreate.png){width=inherit} | `lvglSwitchCreate` | Create a switch. |
| ![](all_blocks/lvglTextareaCreate.png){width=inherit} | `lvglTextareaCreate` | Create a text area. |
| ![](all_blocks/lvglTextareaSetText.png){width=inherit} | `lvglTextareaSetText` | Set text-area text. |
| ![](all_blocks/lvglDropdownCreate.png){width=inherit} | `lvglDropdownCreate` | Create a dropdown. |
| ![](all_blocks/lvglDropdownSetOptions.png){width=inherit} | `lvglDropdownSetOptions` | Set dropdown options. |
| ![](all_blocks/lvglRollerCreate.png){width=inherit} | `lvglRollerCreate` | Create a roller. |
| ![](all_blocks/lvglRollerSetOptions.png){width=inherit} | `lvglRollerSetOptions` | Set roller options. |
| ![](all_blocks/lvglImageCreate.png){width=inherit} | `lvglImageCreate` | Create an image. |
| ![](all_blocks/lvglImageSetSrc.png){width=inherit} | `lvglImageSetSrc` | Set image source. |
| ![](all_blocks/lvglImageSetSrcCostume.png){width=inherit} | `lvglImageSetSrcCostume` | Set image source from a costume. |
| ![](all_blocks/lvglLedCreate.png){width=inherit} | `lvglLedCreate` | Create an LED widget. |
| ![](all_blocks/lvglLedOn.png){width=inherit} | `lvglLedOn` | Turn the LED widget on. |
| ![](all_blocks/lvglLedOff.png){width=inherit} | `lvglLedOff` | Turn the LED widget off. |
| ![](all_blocks/lvglLedToggle.png){width=inherit} | `lvglLedToggle` | Toggle the LED widget. |
| ![](all_blocks/lvglLedSetBrightness.png){width=inherit} | `lvglLedSetBrightness` | Set LED-widget brightness. |
| ![](all_blocks/lvglKeyboardCreate.png){width=inherit} | `lvglKeyboardCreate` | Create a keyboard. |
| ![](all_blocks/lvglKeyboardSetTextarea.png){width=inherit} | `lvglKeyboardSetTextarea` | Bind keyboard to a text area. |
| ![](all_blocks/lvglTabviewCreate.png){width=inherit} | `lvglTabviewCreate` | Create a tab view. |
| ![](all_blocks/lvglTabviewAddTab.png){width=inherit} | `lvglTabviewAddTab` | Add a tab. |
| ![](all_blocks/lvglSetBgColor.png){width=inherit} | `lvglSetBgColor` | Set background colour. |
| ![](all_blocks/lvglSetTextColor.png){width=inherit} | `lvglSetTextColor` | Set text colour. |
| ![](all_blocks/lvglSetOpacity.png){width=inherit} | `lvglSetOpacity` | Set opacity. |
| ![](all_blocks/lvglSetStyleTextFont.png){width=inherit} | `lvglSetStyleTextFont` | Set the text font style. |
| ![](all_blocks/lvglSetStyleBgOpa.png){width=inherit} | `lvglSetStyleBgOpa` | Set the background-opacity style. |
| ![](all_blocks/lvglSetStyleRadius.png){width=inherit} | `lvglSetStyleRadius` | Set the corner-radius style. |
| ![](all_blocks/lvglSetStylePad.png){width=inherit} | `lvglSetStylePad` | Set the padding style. |
| ![](all_blocks/lvglSetStyleBorderWidth.png){width=inherit} | `lvglSetStyleBorderWidth` | Set the border-width style. |
| ![](all_blocks/lvglSetStyleBorderColor.png){width=inherit} | `lvglSetStyleBorderColor` | Set the border-colour style. |
| ![](all_blocks/lvglSetStyleShadowWidth.png){width=inherit} | `lvglSetStyleShadowWidth` | Set the shadow-width style. |
| ![](all_blocks/lvglSetStyleShadowColor.png){width=inherit} | `lvglSetStyleShadowColor` | Set the shadow-colour style. |
| ![](all_blocks/lvglColorHex.png){width=inherit} | `lvglColorHex` | Make a colour from a hex value. |
| ![](all_blocks/lvglGetDisplay.png){width=inherit} | `lvglGetDisplay` | Get the display handle. |
| ![](all_blocks/lvglAddEventCb.png){width=inherit} | `lvglAddEventCb` | Add an event callback. |
| ![](all_blocks/lvglSpinnerCreate.png){width=inherit} | `lvglSpinnerCreate` | Create a spinner. |
| ![](all_blocks/lvglChartCreate.png){width=inherit} | `lvglChartCreate` | Create a chart. |
| ![](all_blocks/lvglChartAddSeries.png){width=inherit} | `lvglChartAddSeries` | Add a chart series. |
| ![](all_blocks/lvglChartSetPoint.png){width=inherit} | `lvglChartSetPoint` | Set a chart point. |
| ![](all_blocks/lvglMeterCreate.png){width=inherit} | `lvglMeterCreate` | Create a meter. |
| ![](all_blocks/lvglAddFlag.png){width=inherit} | `lvglAddFlag` | Add an object flag. |
| ![](all_blocks/lvglClearFlag.png){width=inherit} | `lvglClearFlag` | Clear an object flag. |
| ![](all_blocks/lvglRemoveFlag.png){width=inherit} | `lvglRemoveFlag` | Remove an object flag. |
| ![](all_blocks/lvglAnimCreate.png){width=inherit} | `lvglAnimCreate` | Create an animation. |
| ![](all_blocks/lvglAnimInit.png){width=inherit} | `lvglAnimInit` | Initialise an animation. |
| ![](all_blocks/lvglAnimSetVar.png){width=inherit} | `lvglAnimSetVar` | Set the animation target. |
| ![](all_blocks/lvglAnimSetTime.png){width=inherit} | `lvglAnimSetTime` | Set the animation duration. |
| ![](all_blocks/lvglAnimSetValues.png){width=inherit} | `lvglAnimSetValues` | Set the animation start/end. |
| ![](all_blocks/lvglAnimStart.png){width=inherit} | `lvglAnimStart` | Start an animation. |
| ![](all_blocks/lvglObjDelete.png){width=inherit} | `lvglObjDelete` | Delete an object. |
| ![](all_blocks/lvglObjClean.png){width=inherit} | `lvglObjClean` | Remove an object's children. |
| ![](all_blocks/lvglObjInvalidate.png){width=inherit} | `lvglObjInvalidate` | Mark an object for redraw. |
| ![](all_blocks/lvglCanvasCreate.png){width=inherit} | `lvglCanvasCreate` | Create a canvas. |
| ![](all_blocks/lvglCanvasSetBuffer.png){width=inherit} | `lvglCanvasSetBuffer` | Set the canvas buffer. |
| ![](all_blocks/lvglCanvasFillBg.png){width=inherit} | `lvglCanvasFillBg` | Fill the canvas background. |
| ![](all_blocks/lvglCanvasSetPx.png){width=inherit} | `lvglCanvasSetPx` | Set a canvas pixel. |
| ![](all_blocks/lvglTickInc.png){width=inherit} | `lvglTickInc` | Advance the LVGL tick counter. |

## Pin

> ![](hardblock/hardblock_Pin.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/pin.png){width=inherit} | `pin` | Create a `Pin` with a direction. |
| ![](all_blocks/pin2.png){width=inherit} | `pin2` | Create a `Pin` with input + pull type. |
| ![](all_blocks/on.png){width=inherit} | `on` | Drive the pin high. |
| ![](all_blocks/off.png){width=inherit} | `off` | Drive the pin low. |
| ![](all_blocks/pinValue.png){width=inherit} | `pinValue` | Read the pin value. |
| ![](all_blocks/uartInit.png){width=inherit} | `uartInit` | Initialise a UART. |
| ![](all_blocks/uartRead.png){width=inherit} | `uartRead` | Read bytes from UART. |
| ![](all_blocks/uartWrite.png){width=inherit} | `uartWrite` | Write to UART. |
| ![](all_blocks/neoPixel.png){width=inherit} | `neoPixel` | Create a NeoPixel strip. |
| ![](all_blocks/neoPixelWrite.png){width=inherit} | `neoPixelWrite` | Set and write a NeoPixel colour. |

## Timer

> ![](hardblock/hardblock_Timer.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/timerInit.png){width=inherit} | `timerInit` | Create a `Timer`. |
| ![](all_blocks/timerStart.png){width=inherit} | `timerStart` | Start a periodic/one-shot timer. |
| ![](all_blocks/timerStop.png){width=inherit} | `timerStop` | De-initialise the timer. |

## PWM

> ![](hardblock/hardblock_PWM.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/pwmInit.png){width=inherit} | `pwmInit` | Create a PWM on a pin. |
| ![](all_blocks/pwmSetFreq.png){width=inherit} | `pwmSetFreq` | Set PWM frequency. |
| ![](all_blocks/pwmSetDuty.png){width=inherit} | `pwmSetDuty` | Set PWM duty cycle. |
| ![](all_blocks/pwmDeinit.png){width=inherit} | `pwmDeinit` | De-initialise PWM. |

## ADC

> ![](hardblock/hardblock_ADC.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/adcInit.png){width=inherit} | `adcInit` | Create an ADC on a pin. |
| ![](all_blocks/adcRead.png){width=inherit} | `adcRead` | Read the ADC. |
| ![](all_blocks/dacInit.png){width=inherit} | `dacInit` | Create a DAC on a pin. |
| ![](all_blocks/dacWrite.png){width=inherit} | `dacWrite` | Write to the DAC. |

## SPI

> ![](hardblock/hardblock_SPI.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/spiInit.png){width=inherit} | `spiInit` | Create a hardware SPI. |
| ![](all_blocks/spiBusInit.png){width=inherit} | `spiBusInit` | Initialise an SPI bus. |
| ![](all_blocks/spiRead.png){width=inherit} | `spiRead` | Read from SPI. |
| ![](all_blocks/spiWrite.png){width=inherit} | `spiWrite` | Write to SPI. |
| ![](all_blocks/spiReadWrite.png){width=inherit} | `spiReadWrite` | Full-duplex read into a buffer. |

## I2C

> ![](hardblock/hardblock_I2C.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/i2cInit.png){width=inherit} | `i2cInit` | Create an I²C bus. |
| ![](all_blocks/i2cScan.png){width=inherit} | `i2cScan` | Scan for I²C addresses. |
| ![](all_blocks/i2cRead.png){width=inherit} | `i2cRead` | Read from a device. |
| ![](all_blocks/i2cWrite.png){width=inherit} | `i2cWrite` | Write to a device. |

## WatchDog (RTC, WDT, deep sleep)

> ![](hardblock/hardblock_WatchDog.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/rtcInit.png){width=inherit} | `rtcInit` | Create an `RTC`. |
| ![](all_blocks/rtcSetTime.png){width=inherit} | `rtcSetTime` | Set the RTC datetime. |
| ![](all_blocks/rtcGetTime.png){width=inherit} | `rtcGetTime` | Get the RTC datetime tuple. |
| ![](all_blocks/rtcGetYear.png){width=inherit} | `rtcGetYear` | Get the year. |
| ![](all_blocks/rtcGetMonth.png){width=inherit} | `rtcGetMonth` | Get the month. |
| ![](all_blocks/rtcGetDay.png){width=inherit} | `rtcGetDay` | Get the day. |
| ![](all_blocks/rtcGetHour.png){width=inherit} | `rtcGetHour` | Get the hour. |
| ![](all_blocks/rtcGetMinute.png){width=inherit} | `rtcGetMinute` | Get the minute. |
| ![](all_blocks/rtcGetSecond.png){width=inherit} | `rtcGetSecond` | Get the second. |
| ![](all_blocks/wdtInit.png){width=inherit} | `wdtInit` | Create a watchdog timer. |
| ![](all_blocks/wdtFeed.png){width=inherit} | `wdtFeed` | Feed the watchdog. |
| ![](all_blocks/deepSleep.png){width=inherit} | `deepSleep` | Enter deep sleep for a duration. |

## SD Card

> ![](hardblock/hardblock_SDcard.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/sdCardInit.png){width=inherit} | `sdCardInit` | Create an `SDCard`. |
| ![](all_blocks/sdCardMount.png){width=inherit} | `sdCardMount` | Mount the card. |
| ![](all_blocks/sdCardUnmount.png){width=inherit} | `sdCardUnmount` | Unmount the card. |
| ![](all_blocks/sdCardFileWrite.png){width=inherit} | `sdCardFileWrite` | Write a file to the card. |
| ![](all_blocks/sdCardFileRead.png){width=inherit} | `sdCardFileRead` | Read a file from the card. |

## RMT

> ![](hardblock/hardblock_RMT.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/rmtInit.png){width=inherit} | `rmtInit` | Create an RMT channel. |
| ![](all_blocks/rmtWrite.png){width=inherit} | `rmtWrite` | Write RMT pulses. |
| ![](all_blocks/rmtDeinit.png){width=inherit} | `rmtDeinit` | De-initialise RMT. |

## One-Wire

> ![](hardblock/hardblock_OneWire.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/oneWireInit.png){width=inherit} | `oneWireInit` | Create a OneWire bus. |
| ![](all_blocks/oneWireScan.png){width=inherit} | `oneWireScan` | Scan for OneWire devices. |
| ![](all_blocks/oneWireRead.png){width=inherit} | `oneWireRead` | Read a byte. |
| ![](all_blocks/oneWireWrite.png){width=inherit} | `oneWireWrite` | Write a byte. |

## Capacitive Touch

> ![](hardblock/hardblock_Touch.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/touchInit.png){width=inherit} | `touchInit` | Create a `TouchPad`. |
| ![](all_blocks/touchRead.png){width=inherit} | `touchRead` | Read the touch value. |

## DHT

> ![](hardblock/hardblock_DHT.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/dhtInit.png){width=inherit} | `dhtInit` | Create a DHT sensor. |
| ![](all_blocks/dhtReadTemperature.png){width=inherit} | `dhtReadTemperature` | Measure and read temperature. |
| ![](all_blocks/dhtReadHumidity.png){width=inherit} | `dhtReadHumidity` | Measure and read humidity. |

## HC-SR04 Sonar

> ![](hardblock/hardblock_Sonar.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/hcsr04Init.png){width=inherit} | `hcsr04Init` | Define the driver and create an HC-SR04 sensor. |
| ![](all_blocks/hcsr04DistanceCm.png){width=inherit} | `hcsr04DistanceCm` | Read distance in centimetres. |
| ![](all_blocks/hcsr04DistanceMm.png){width=inherit} | `hcsr04DistanceMm` | Read distance in millimetres. |

## Sensors

> ![](hardblock/hardblock_Sensors.png){width=inherit}

| Image | Block `type` | Description |
| --- | --- | --- |
| ![](all_blocks/temperature.png){width=inherit} | `temperature` | Read an analog thermistor via `getTemperature`. |
| ![](all_blocks/fourDigitDisplay.png){width=inherit} | `fourDigitDisplay` | Create a TM1637 4-digit display. |
| ![](all_blocks/fourDigitDisplay_setNumber.png){width=inherit} | `fourDigitDisplay_setNumber` | Show a number on the display. |
| ![](all_blocks/motor.png){width=inherit} | `motor` | Create a DC-motor control pin. |
| ![](all_blocks/motorOn.png){width=inherit} | `motorOn` | Turn the motor on. |
| ![](all_blocks/motorOff.png){width=inherit} | `motorOff` | Turn the motor off. |
| ![](all_blocks/servo.png){width=inherit} | `servo` | Create a servo. |
| ![](all_blocks/servoAngle.png){width=inherit} | `servoAngle` | Set the servo angle. |

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
