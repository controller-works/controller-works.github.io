---
permalink: /mini42/firmware/
date: 2022-10-02 01:01:00
---
# Firmware
The easiest way to customize your keyboard is to use the pre-loaded firmware and apply a custom keymap using the Via app.

Another option is to load custom firmware.
* Vial firmware allows on-the-fly reconfiguration of keymaps and other keyboard functions. It is based on a fork of QMK, so a special firmware image must be loaded to utilize the Vial app.
* Custom firmware with a custom keymap can be created using the [QMK Online Configurator](https://config.qmk.fm/#/) You must enter bootloader mode on your keyboard to load new firmware.

## Pre-Loaded Firmware
The mini42 comes with an official build of QMK Via firmware pre-installed. Follow these steps to view and edit your keymap using the Via application.
1. Plug your keyboard into your computer or other host system.
1. Navigate to https://usevia.app/#/ using a web browser such as Chrome or a browser based on Chrome with HID support (this allows the web app to communicate directly with your keyboard).
1. Press `Authorize Device +`. A dialog should appear with `Controller Works mini42` listed. Select that device and press `Connect`. The mini42 keymap should appear.
1. Select the layer in the upper right quadrant of the app. Layers are sets of keyboard functions that are accessible through shifting the keyboard to that layer, similar to standard shift keys. The different key categories are listed in the lower left quadrant. There are many ways to access different layers. A good starting point is `Fn1(Fn3)` and `Fn2(Fn3)`. These will select layer 1 and layer 2 if held down individually, and layer 3 if held down together. Make sure the same keys in the upper layers are set to `KC_TRNS` or the downward facing triangle `▼`.

## Bootloader
Enter the bootloader in 3 ways:
* **Bootmagic reset**: Hold down the upper left key on the left hand keyboard half or the upper right key on the right hand keyboard half while plugging in USB
* **Physical reset button**: Press the RST button twice, rapidly. The RST button can only be pressed using a narrow object such as a toothpick to prevent accidental activation.
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available

## Pre-Built Firmware
Get into bootloader mode (see above). The keyboard will appear as a USB drive on your host machine. Drag one of the .UF2 files below onto the USB drive. Plug the USB into the other half of the keyboard and repeat the process.

[mini42 default firmware Via uf2 file](https://raw.githubusercontent.com/the-via/firmware/master/controllerworks_mini42_via.uf2) **Use this if in doubt** Works with [Via app](https://usevia.app/#/)

[mini42 default firmware Vial uf2 file](/assets/controllerworks_mini42_vial.uf2) Works with [Vial app](https://vial.rocks/)

## Build Your Own Firmware (Advanced)
The mini42 is officially supported in QMK. Please follow [these instructions](https://docs.qmk.fm/#/newbs_getting_started) to build and customize your own firmware for the mini42.

The mini42 is also supported in the Vial fork of QMK. Please follow [these instructions](https://get.vial.today/) for using and customizing Vial.