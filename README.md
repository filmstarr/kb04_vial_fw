# kb04_vial_fw
Compiled firmware for DOIO's kb04 (aka Megalodon Knob Pad/Megalodon Macro Pad with a Knob) along with original source code for vial-qmk.

![doio/kb04](https://cdn.shopify.com/s/files/1/0463/5980/6101/products/4_f40396cc-ea72-47a5-887f-bbeeb4023b11_1100x.png?v=1654787686)

A macropad that has a 4-key keyboard made by DOIO, controlled by an APM32F103CBT6 chipset. The keyboard features per-key RGB and 1 encoder.

There are three keymaps: default, vial, and vial-inverted. vial-inverted is intended for use when the keyboard is plugged in upside down (with the encoder at the top).

* Keyboard Maintainer: [filmstarr](https://github.com/filmstarr)
* Hardware Supported: DOIO Knob Board - KB04
* Hardware Availability: [keebmonkey.com](https://www.keebmonkey.com/products/megalodon-macro-pad-with-a-knob)

Advantage over stock firmware.

* Embeded layout so no need for sideloading json
* Native encoder layout
* Vial specific feature like macro delay
* RGB
* The knob now correctly emits 20 pulse per revolution, matching the dedent
* Fix layout issues causing keymap to display incorrectly in Via/Vial

## Building

Make example for this keyboard (after setting up your build environment):

    make doio/kb04:vial

Flashing example for this keyboard:

    make doio/kb04:vial:flash

See [Vial QMK](https://get.vial.today/docs/porting-to-vial.html) for details on Vial QMF fork and porting to Vial.

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).


## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down the key at (0,0) in the matrix (1! key) and plug in the keyboard
* **Physical reset button**: Briefly press the button on the back of the PCB
* **Keycode in layout**: Press the key mapped to `QK_BOOT` if it is available
