---
title: Setup Your Board
description: >-
  How the Board Works, and how to Setup Yours
---


# Setup Instructions
To get your board to work, you only need to provide it with power and WiFi information.

### Power
Boards can be powered with a USB-C cable **or** a battery with a JST-PH 2.0 connector. Either power source must provide 5 volts (5V) of power - providing more volts may damage your board, and fewer may cause LEDs to dim or blink out.

The simplest power source is a USB-C cable attached to a phone charger or computer. Be sure to check your power supply, but most chargers will provide 5V.

Alternatively, you can use a battery or alternative power supply that provides approximately 5V of power through a JST-PH 2.0 connection. For example, a [3x AA battery holder](https://www.adafruit.com/product/4779) will provide sufficient power with three fully charged batteries.
**Caution**: Batteries may drain quickly when powering the board alone. For continuous use, a stable power supply is recommended.

You may also power your board using both the USB-C and JST connections. Doing so should draw less power from both supplies.

1. Download [Arduino IDE](https://www.arduino.cc/en/software)
2. Download the [dctransistor code](https://github.com/LArkema/dctransistor-project)
3. Download required support software and libraries
    1. [Add ESP8266 Board to Arduino](https://arduino-esp8266.readthedocs.io/en/latest/installing.html#instructions)
    2. Add ArduinoJson and Adafruit_NeoPixel [libraries to Arduino](https://docs.arduino.cc/software/ide-v1/tutorials/installing-libraries)
4. (Optional) [Register](https://developer.wmata.com/signup/) for a WMATA API Key (if you want to monitor how your board uses WMATA data)
5. Modify the `arduino_secrets.h` file with your WiFi SSID and Password and your WMATA API key, if you want to use your own
6. Plug in the board to your computer and [upload](https://docs.arduino.cc/software/ide-v2/tutorials/getting-started/ide-v2-uploading-a-sketch) the dctransistor sketch
    1. Make sure you have selected the ESP8266 board, a 9600 baud rate, and the correct COM port for the board in Arduino's `Tools` menu.

<figure class="led-pic">
<img src="{{ site.baseurl }}/images/board-regular-night.jpg" alt="Picture of a DCtransistor board shot in the dark to show the different LED colors. As a result, the details of the board are not visible, except for the rivers." style="width: 275px; height: auto;">
<figcaption>Board in the dark to show LED colors</figcaption>
</figure>

### Customize Your Board
The main code (`.ino`) file sets a number of configuration values, most of which will break the board's functionality if they are changed. However, the configuration values for each line (starting around line 60) have their LED color
defined with a `<line_code>_HEX_COLOR` 32-bit WRGB hex value, which you can change to whatever colors you want. In addition, `all_lines` array, defined right before the `setup()` function defines the order for what color a station LED will turn if two trains from different lines are "at" the same station (going opposite directions, one right behind another, etc.). You can change the order if you're partial to one line over another.

### Power Your Board
<div class="pwr-pics">
<figure class="first-pwr-pic">
<img src="{{ site.baseurl }}/images/usb-power-board.jpg" alt="Picture of a DCTransistor board in the middle of a loop through a program that displays a rainbow on the board. On the left side of the picture, a Micro-USB cable is plugged into the chip on the back of the board." style="width: 300px; height: auto;">
<figcaption>Board powered by a Micro-USB cable</figcaption>
</figure>

<figure>
<img src="{{ site.baseurl }}/images/bat-power-board.jpg" alt="Picture of a DCTransistor board displaying live train positions. The battery holder on the bottom-left of the board holds 3 AA batteries." style="width: 300px; height: auto;">
<figcaption>Board powered by 3 AA batteries</figcaption>
</figure>
</div>
Boards can either be powered through a Micro-USB cable *OR* 3 AA batteries. While you must use a USB cable connected to a computer to load the software, you can then use a cable from a phone charger or other direct power supply as long as it supplies power at (or near) 5 Volts (more than 5V may permanently damage the chip or LEDs on the board). 

You can also power the board using 3 AA batteries, which are controlled with an "On/Off" switch. If using batteries, make *sure* the power switch is set to "Off" while inserting the batteries. For additional protection, begin inserting batteries from the bottom up, as the bottom battery grounds the board while the top battery connects to power. Providing power via the top battery without a connection to ground may also cause permanent damage to the board. 

Finally, DO NOT CONNECT THE BOARD TO USB AND BATTERY POWER AT THE SAME TIME. This will provide far more power than the chip or LEDs are able to handle, and again may cause permanent damage. While it is possible to leave batteries in the board with the switch turned off while connected to a USB power supply, I recommend taking at least the top battery out to ensure extra voltage isn't supplied to the board.  

<style>
  .pwr-pics {
    margin: auto;
    float: left;
  }
  .led-pic {
    float: right;
  }
</style>
<br>

## How It Works

<img class="cover-board" src="{{ site.baseurl }}/images/board-basic.jpg" alt="Large picture of a DCTransistor board, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map.">

Boards work by getting real-time train positions WMATA makes available through it's [API](https://developer.wmata.com/docs/services/5763fa6ff91823096cac1057/operations/5763fb35f91823096cac1058), and turning on LEDs for the station a train is arriving at or has most recently left from. 

When the board turns on, it turns all LEDs off except the power LED (some other LEDs may flash on with instructions from before the board turned off), then attempts to connect WiFi. At this point, the WiFi LED will turn yellow until it successfully connects (which may take a few seconds), and then it will turn green. The board then attempts to connect to the WMATA API, and the Web LED will turn yellow until it successfully receives the first batch of train positions.

WMATA provides a list of every train in service, the line it's on, and which circuit (i.e. track segment) it's currently on. For each train, the board checks which stations the train is between, including if it's arriving at a station (currently using two circuits before a station as "arriving"); and records that the train's line has a train at that station. After going through all active train positions, the board goes through all stations and sees if any line has a train "at" each station, setting the LED for that station to the line's color if there is and turning the LED off if not. The board then updates all LEDs to show the new positions, and waits twenty seconds before getting new train positions from WMATA.

***Important:*** Train positions are taken directly from WMATA, and are only as accurate as the location data WMATA provides. In particular, WMATA may report a train's position "at" a station that is closed for repairs, or "at" the station before a series of closed stations long after a train has left. Further, a circuit is not a uniform measurement, so while a train may move on the board because it is two circuits away from the station it may not be close enough for an "ARR" message to appear at a station. Finally, the board has LEDs for stations that are not yet open as of July 2022 (i.e. Potomac Yard and the Silver Line Expansion), and therefore do not turn on. I will try to release software updates as soon as the stations open, but make no guarantees on timeliness. You are responsible for updating your board with any new software, though I will try to maintain voluntary notification emails.

## Coming Changes
There will likely be some differences with the prototype board and the production board. You can see some of the (likely) changes on the [waitlist](/waitlist/) page and recommend your own.