# Keychron K3 Max

![Keychron K3 Max](https://cdn.shopify.com/s/files/1/0059/0630/1017/files/Keychron-K3-Max-wireless-mechanical-keyboard.jpg?v=1699931171)

A customizable 84 keys TKL keyboard.

* Keyboard Maintainer: [Keychron](https://github.com/keychron)
* Hardware Supported: Keychron K3 Max
* Hardware Availability: [Keychron K3 Max QMK/VIA Wireless Custom Mechanical Keyboard](https://www.keychron.com/products/keychron-k3-max-qmk-via-wireless-custom-mechanical-keyboard)

Make example for this keyboard (after setting up your build environment):

    make keychron/k3_max/ansi/rgb:default
    make keychron/k3_max/ansi/white:default

Flashing example for this keyboard:

    make keychron/k3_max/ansi/rgb:default:flash
    make keychron/k3_max/ansi/white:default:flash

**Reset Key**: Disconnect the USB cable, toggle mode switch to "Cable", hold down the *Esc* key or reset button underneath space bar, then connect the USB cable.

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).


### Flashing the keyboard with new firmware

> The original cable should be used to flash the firmware.
> See the original [Keychron manual](https://www.keychron.com/pages/firmware-and-json-files-of-the-keychron-qmk-k-pro-and-k-max-series-keyboards#:~:text=How%20to%20flash%20the%20keyboard%20firmware%20with%20the%20QMK%20toolbox)

1. Set the keyboard mode to `Cable` and `Mac` (when building on Mac) 

1. Build the **K3 max** keyboard firmware using:

    ```bash
    make keychron/k3_max/ansi/rgb:default
    ```

1. Unplug the cable from the keyboard

1. Open the [QMK Toolbox](https://qmk.fm/toolbox)

1. Remove the space bar keycap and **press and hold the reset button** on the left side of the space bar switch on the PCB.

1. Plug in the cable **while still holding the reset button**. Do not release the reset button till the QMK Toolbox display in yellow words "***DFU device connected". 

1. Click open and choose the firmware located in `.build/keychron_k3_max_ansi_rgb_default.bin`. Click the Flash button. It will start flashing. (Note: Do NOT unplug the power cable while it's flashing.)

1. Wait a few seconds and when you see the `Flash complete`, it means the keyboard has flashed successfully. 