# ZMK support for the YamPAD
The goal of this project was to create wireless support for the YamPAD macropad using ZMK. The creator of the YamPAD originally intended wired compatability with QMK flashing. 

If you are not familiar with [ZMK](https://zmk.dev/docs) I highly suggest that you take a look at the documentation to familiarize yourself with the installation process. The YamPAD is not included in ZMK's list of supported shields, so we have to build our own firmware. I suggest following [this guide](https://zmk.dev/docs/development/new-shield) to accomplish this.

This repo contains all the necessary files to build the .uf2 file to flash on the MCU. Once flashed, the macropad should be ready to use. You can use GitHub Actions to build your own firmware, but if you run into issues with that, you could also create a [local build](https://zmk.dev/docs/development/setup) on your machine.

### Requirements
[YamPAD PCB](https://hackaday.io/project/163491-yampad-feature-packed-open-source-macropad)

[nice!nano](https://nicekeyboards.com/)

- Alternatives: [ProMicro NRF52840](https://github.com/joric/nrfmicro/wiki/Alternatives#supermini-nrf52840)

I went with the ProMicro NRF52840

## [Releases](https://github.com/curserat/yampad-module/releases)
### Features
- Bluetooth
- OLED Display
- Keymap Layers (Modifiable)

RGB support is soon to be added

### Notes
- ZMK comes with it's own OLED configuration. Currently, there is not sufficient documentation to create custom displays. [See](https://zmk.dev/docs/features/displays)
- For wireless macropads, an OLED display is not recommended because it will greatly drain the battery. However, you could go with the [nice!view display](https://nicekeyboards.com/nice-view) which has a much lower power draw.
- Check for any hardware issues: diodes, switches, connections, etc.

## Resources
The [YamPAD](https://hackaday.io/project/163491-yampad-feature-packed-open-source-macropad) is an open source macropad by [Mattia Dal Ben](https://github.com/mattdibi)

[ZMK Firmware](https://zmk.dev/) is an open source (MIT) keyboard firmware built on the [Zephyr™ Project](https://zephyrproject.org/) Real Time Operating System (RTOS). ZMK's goal is to provide a modern, wireless, and powerful firmware free of licensing issues.
