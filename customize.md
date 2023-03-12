---
title: Customize Your Board
description: >-
  Change your board's display and firmware
---

## Prerequisite Tools and Software

1. Download the [Arduino IDE](https://www.arduino.cc/en/software)
2. Download the [dctransistor code](https://github.com/LArkema/dctransistor-project)
3. Download required support software and libraries
    1. [Add ESP8266 Board to Arduino](https://arduino-esp8266.readthedocs.io/en/latest/installing.html#instructions)
    2. Add the ArduinoJson, WiFiManager, and Adafruit_NeoPixel [libraries to Arduino](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries)
4. [Register](https://developer.wmata.com/signup/) for a WMATA API Key (if you want to monitor how your board uses WMATA data)
5. Modify the `DCTransistor/config.h` file with your changes and WMATA API key
6. Plug in the board to your computer and [upload](https://docs.arduino.cc/software/ide-v2/tutorials/getting-started/ide-v2-uploading-a-sketch) the dctransistor sketch
    1. Make sure you have selected the ESP8266 board, a 9600 baud rate, and the correct COM port for the board in Arduino's `Tools` menu.


### Customize Your Board
The board is powered by an ESP-12F chip (ESP8266 platform) and WS2812B LEDs that function with the Arduino NeoPixel library. Using some of the code on [GitHub](https://github.com/LArkema/dctransistor-project/tree/main), you can upload your own code that makes the board behave however you want. More details on how deep board customizations are 

There are also simpler customizations you can make to the DCTransistor display. The configuration file (`config.h`) sets a number of configuration values, such as the brightness of the LEDs and the exact color used to represent each line. When customizing the board's configuration values, pay attention to the values that are mostly aesthetic and the ones that may break the board's functionality.