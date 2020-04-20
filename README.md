# Buzzer 2.0

**Buzzers have not been upgraded to 2.0 yet!**

This is the repository for the the hardware of the internal buzzer system at the CoMakingSpace. The old 1.0 version worked ~~great~~ well enough, but had some functionality limitations such as cumbersome firmware updates and outdated MiFare classic implementation.
The security element is not as important for the indoor system, but nice to have.

For software implementation details go to the dedicated software repo (**ToDo** add link).

## Changes from version 1.0

* Switch to ESP32 module for future BLE implementations
  * much better security features and OTA possibility
  * MicroPython support
* Ditching the additional PN532 module for an in board implementation
  * larger antenna *should* allow for better range
  * MiFare Desfire EV1 support
* buck converter with input protection
  * 5-17V input (as long as the buzzer still activates)
* **RGB LEDs!**
* Case-entry contacts
* single board design


## Cloning repo

`git clone --recurse-submodules ....`

## Subcircuits

### PN532

The schematic and and layout were closely taken from Adafruit's PN532 v1.6 breakout board. The component values of the antenna matching circuit may need to be adjusted once the boards are assembled in case the resonance frequency deviated strongly from the standard 13.56MHz.
