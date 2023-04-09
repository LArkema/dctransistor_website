---
title: Board Details
description: >-
  Product Specifications and Software Summary
---

<img class="cover-board" src="{{ site.baseurl }}/images/lightup-board.jpg" alt="Large picture of a DCTransistor board, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map.">

<div style="outline-style: solid; overflow: hidden">
  <h2>Board Specifications</h2>
  <div class="column">
    <ul>
      <li>105 RGB (Red Green Blue) LEDs</li>
      <li>20 second LED refresh rate</li>
      <li>1x ESP-12F WiFi module and processor</li>
      <li>1x CH340C USB-to-serial conversion chip</li>
      <li>12" x 12.4" (304.8 x 314.8mm)</li>
    </ul>
  </div>
  <div class="column">
    <ul>
      <li>Requires 5 Volts (5V) power (supply not included)</li>
      <li>USB-C power and data port</li>
      <li>JST PH-2.0 power connector</li>
      <li>On/Off switch</li>
      <li>2x 5.5mm mounting holes</li>
    </ul>
  </div>
  <h3 style="padding-left: 20px;">Key Open Source Libraries</h3>
    <ul>
      <li><a href="https://github.com/esp8266/Arduino">ESP8266 Arduino Core</a></li>
      <li><a href="https://www.arduino.cc/en/software">Arduino IDE and Main Libraries</a></li>
      <li><a href="https://github.com/adafruit/Adafruit_NeoPixel/">Adafruit NeoPixel</a></li>
      <li><a href="https://arduinojson.org/">ArduinoJson</a></li>
      <li><a href="https://github.com/tzapu/WiFiManager/">WiFiManager</a></li>
    </ul>
</div>

<style>
  .column {
    float: left;
    width: 50%;
  }

  @media screen and (max-width: 600px) {
  .column {
    width: 100%;
  }
  }
</style>

<p></p>
<br>
## How It Works

Boards work by getting real-time train positions WMATA makes available through it's [API](https://developer.wmata.com/docs/services/5763fa6ff91823096cac1057/operations/5763fb35f91823096cac1058), and turning on LEDs for the station a train is arriving at or most recently departed. 

When the board turns on, all LEDs turn off except the power LED (some other LEDs may flash on with data from before the board turned off), then attempts to connect WiFi. At this point, the WiFi LED will turn yellow until it successfully connects (which may take a few seconds), and then it will turn green. The board then attempts to connect to the WMATA API, and the Web LED will turn yellow until it successfully receives the first batch of train positions.

WMATA provides a list of every train in service and the line and track segment they're on. For each train, the board checks which stations the train is between, including if it's arriving at a station (currently using two segments before a station as "arriving"); and records that the train's line has a train at that station. After going through all active train positions, the board goes through all stations and sees if any line has a train "at" the station. If a line has a train "at" the station, the LED turns on to that line's color, and turns off if no line has a train there. The board then updates all LEDs to show the new positions, and waits twenty seconds before getting new train positions from WMATA.

***Important:*** Train positions are taken directly from WMATA, and are only as accurate as the location data WMATA provides. In particular, WMATA may report a train's position "at" a station that is closed for repairs, or "at" the station before a series of closed stations long after a train has left. Further, a segment is not a uniform measurement, so while a train may move on the board because it is two circuits away from the station it may not be close enough for an "ARR" message to appear at a station. Finally, the board has LEDs for stations that are not yet open as of April 2023 (i.e. Potomac Yard), and therefore do not turn on. I will try to release software updates as soon as the stations open, but make no guarantees on timeliness. While boards have an auto-update feature, the software is provided as-is and comes with no guarantees or warrantees.

### Old Boards
The current version of the board got here through prototyping and trial and error. If you're interested in prior versions of the board, or have one you want to update, see [Old Boards](/old-boards)