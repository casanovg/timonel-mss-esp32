# timonel-mss-esp32
## Timonel I2C master single slave test for ESP32

This ESP32/Arduino test application [shows](http://youtu.be/-7GOMToGvzI) the usage of TWI master libraries.

It is a serial console-based application that allows sending commands to a device that runs the [Timonel bootloader](https://github.com/casanovg/timonel). Its main functions are:

* Searches a device running Timonel bootloader on the TWI bus and initializes it.
* Uploads an application to the device. The application to send to the AVR bootloader (payload) is compiled as part of this TWI master application. The utility "timonel-hexparser" is used to convert an AVR application into a TWI master payload.
* Deletes the application from the AVR device memory.
* Optionally, it makes an on-screen dump of all the device's memory for debugging.

The application has been tested on a [DOIT ESP32 DevKit V1 module](https://github.com/casanovg/timonel-mss-esp32/blob/media/DOIT-ESP32-DevKit-V1-Pinout.png). It is compiled and flashed to the device using [PlatformIO](http://platformio.org) over [VS Code](http://code.visualstudio.com).