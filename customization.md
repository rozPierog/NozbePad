## Creating keymaps
![How to short pins](/resources/qmkConfigurator.png)

- Go to [QMK Configurator](https://config.qmk.fm/#/handwired/nozbe_macro/LAYOUT) and select `KEYBOARD: handwired/nozbe_macro` and `LAYOUT: LAYOUT` _(1)_
- Click on key you want _(2)_ to modify and press key you want to assign on your keyboard

  OR
- Click on key you want _(2)_ to modify and scroll down to `KEYCODES` _(3)_ section and pick a key you want to assign from table
  - Hover over key to display more information about it
  - In `Quantum` section you can find "advanced" stuff like Layer management and Key Combinations (e.g.. `CTRL` + `SHIFT` + `<some_key>`)
    - some keys can be connected with others, if you hover on such case you will see an explainer
    - Layers allow you to create combinations like `hold key one and tap key 2 to disable backlight` - you can do this with `LT1-15`
    - Easiest way to understand layers is to look at number row at your keyboard. If you press on `2` it's gonna type `2`, but if you hold `SHIFT` and then tap `2` it's gonna type `@`. So `SHIFT` is activating another layer at your keyboard.
    - You can look trough active layers on your keymap with `0`-`15` buttons at the left _(4)_
  - You can find Backlight toggle in `KEYBOARD SETTINGS` > `BACKLIGHT SETTINGS`
- After you are satisfied with your keys, click on `Compile` in top right corner _(5)_
- Wait for potato🥔
- After it's done click on `⬇️FIRMWARE` _(6)_

## Flashing
- Download [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases)
  - find release marked with `Latest`
  - Download right file for your system
    - pkg - macOS
    - exe - windows
    - n/a - Linux (go figure out [QMK CLI](https://beta.docs.qmk.fm/tutorial/newbs_getting_started))
- open it
![qmk toolbox](/resources/qmkToolbox.png)
- in `local file` select file you've downloaded (click on `open`) _(1)_
- connect NozbePad to your computer
- take something that's conductive (screwdriver, screw, even unplugged USB)
- touch `GND` and `RST` pins at the reverse of the NozbePad at the same time (pins 2 and 3 from the top on the right side)
![How to short pins](/resources/howToShort.jpg)
- You should have seen this message in QMK Toolbox
```
*** Caterina device connected: Arduino LLC Arduino Micro
```
- If you got message like below do it again
```
*** Caterina device disconnected: Arduino LLC Arduino Micro
```
- make sure that `MCU (AVR only)` looks like on screenshot above
- Press `FLASH` _(2)_
- That's all!

