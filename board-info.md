---
title: Board Details
description: >-
  Product Specifications and Software Summary
---

**Jump To:**
* [Bidirectional Board](#bidirectional-board)
* [Standard Board](#standard-board)
* [Dev Board](#dev-board)
* [How It Works](#how-it-works)

<p style="color: red"><b>Holiday Pricing + Free Shipping Until 12/16/2024. Orders after 12/16/2024 will not be shipped until 2025.</b></p>
<!-- <p style="color: red"><b>Deliveries Paused From 11/25/2024-12/3/2024. Orders will not be shipped until 12/4/2024.</b></p> -->

# Bidirectional Board

The bidirectional board is here! With 207 individual LEDs, the bidirectional board has separate indicators for trains moving in both directions at each station. Indicators move on the "right" side of the track relative to the train's direction. The bidirectional board takes the DCTransistor boards from a neat aesthetic item to a clearer visual representation of trains moving throughout the Metro system. Enjoy! 

<button class="buybutton"><a href="https://buy.stripe.com/14kaHdcug0hxfjq28c" target="_blank" style="color: inherit">Buy Now (<s>$105</s> $90)</a></button>


<img class="cover-board" src="{{ site.baseurl }}/images/bidirectional_board.jpg" alt="Large picture of a Bidirectional DCTransistor bBard, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map. For each station on the DC Metro map, there are two 2mm LEDs to indicate trains going both directions at each station.">

<div style="outline-style: solid; overflow: hidden">
  <h2>Board Specifications</h2>
  <div class="column">
    <ul>
      <li>207 2mm x 2mm RGB LEDs</li>
      <li>2 second LED refresh rate</li>
      <li>1 ESP-12F WiFi module and processor</li>
      <li>1 CH340C USB-to-serial conversion chip</li>
      <li>12" x 12" (304.8 x 304.8mm)</li>
    </ul>
  </div>
  <div class="column">
    <ul>
      <li>Requires 5 Volts (5V) power (supply not included)</li>
      <li>USB-C power and data port</li>
      <li>On/Off switch</li>
      <li>2 5.5mm mounting holes</li>
    </ul>
  </div>
</div>

<b>

# Standard Board

The "standard board" is the classic DCTransistor board with one LED representing each WMATA station. LED indicators will move in both directions along the single display for both directions of a WMATA line. I have produced multiple batches of the standard board, and in addition to some minor aesthetic adjustments, I removed the JST battery connector from recent versions. If you specifically want a board with a JST connection, email <a href="mailto:orders@dctransistor.com">orders@dctransistor.com</a> when placing your order.

<button class="buybutton"><a href="https://buy.stripe.com/dR616Dam80hx5IQaEG" target="_blank" style="color: inherit">Buy Now (<s>$65</s> $50)</a></button>


<img class="cover-board" src="{{ site.baseurl }}/images/lightup-board.jpg" alt="Large picture of a DCTransistor board, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map.">

<div style="outline-style: solid; overflow: hidden">
  <h2>Board Specifications</h2>
  <div class="column">
    <ul>
      <li>105 5mm x 5mm RGB LEDs</li>
      <li>2 second LED refresh rate</li>
      <li>1 ESP-12F WiFi module and processor</li>
      <li>1 CH340C USB-to-serial conversion chip</li>
      <li>12" x 12" (304.8 x 304.8mm) (304.8 x 314.8 in old versions)</li>
    </ul>
  </div>
  <div class="column">
    <ul>
      <li>Requires 5 Volts (5V) power (supply not included)</li>
      <li>USB-C power and data port</li>
      <li>JST PH-2.0 power connector (only in old versions)</li>
      <li>On/Off switch</li>
      <li>2 5.5mm mounting holes</li>
    </ul>
  </div>
</div>

<br>

# Dev Board

The "dev board" is one of the remaining batch of 10 prototype boards. The Dev board is perfectly functional and works the same as the Standard board, with a few notable differences to aesthetics and interface. The JST connector is replaced with an attached AA battery holder, the ESP32 chip running the board is attached through a separate development board - <u>allowing custom GPIO connections to the chip and board</u>, power is provided by a Micro-USB cable instead of USB-C, and the two side mounting holes are replaced by a single mounting hole in the center of the board. Some of the text on the board is also difficult to read. Also, the LEDs kind of suck and don't some of the line colors. That said, there are only four (4!) left at the time of this writing and they're cheap!

<button class="buybutton"><a href="https://buy.stripe.com/5kA9D965Sfcr2wEfZ3" target="_blank" style="color: inherit">Buy Now ($45)</a></button>

If you own or plan to purchase a dev board, **be sure to read** the information on the <a href="/dev-boards/">dev boards</a> page.

<img class="cover-board" src="{{ site.baseurl }}/images/dev-board-nov-23.jpg" alt="Large picture of a Development DCTransistor board, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map. As an older board, it has far less refined silk screen aesthetics and looks much more shoddy compared to the Bidirectional and Standard boards.">

<div style="outline-style: solid; overflow: hidden">
  <h2>Board Specifications</h2>
  <div class="column">
    <ul>
      <li>105 5mm x 5mm RGB LEDs</li>
      <li>2 second LED refresh rate</li>
      <li>1 ESP-12F Development Board with GPIO pins</li>
      <li>1 CH340C USB-to-serial conversion chip</li>
      <li>12" x 12" (304.8 x 304.8mm)</li>
    </ul>
  </div>
  <div class="column">
    <ul>
      <li>Requires 5 Volts (5V) power (supply not included)</li>
      <li>Micro-USB power and data port</li>
      <li>3 AA Battery Holder</li>
      <li>On/Off switch</li>
      <li>1 6mm mounting hole</li>
    </ul>
  </div>
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

  	.buybutton {
    background-color: #0074d4;
    color: white;
    border: none;
    text-align: center;
    text-decoration: none;
    display: block;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    font-size: 2vw;
    padding: 14px 40px;
    border-radius: 8px;
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
    pointer-events: pointer;
	}

  .buybutton:hover {
    transform: scale(1.05)
  }

  .buybutton-disabled{
    background-color: #808080;
    color: white;
    border: none;
    text-align: center;
    text-decoration: none;
    display: block;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    font-size: 24px;
    padding: 14px 40px;
    border-radius: 8px;
  }
</style>

<br>

## How It Works

Boards work by getting real-time train positions WMATA makes available through it's [API](https://developer.wmata.com/docs/services/5763fa6ff91823096cac1057/operations/5763fb35f91823096cac1058), and turning on LEDs for the station a train is arriving at or most recently departed. 

When the board turns on, all LEDs turn off except the power LED (some other LEDs may flash on with data from before the board turned off), then attempts to connect WiFi. At this point, the WiFi LED will turn yellow until it successfully connects (which may take a few seconds), and then it will turn green. The board then attempts to connect to the WMATA API, and the Web LED will turn yellow until it successfully receives the first batch of train positions.

WMATA provides a list of every train in service and the line and track segment they're on. For each train, the board checks which stations the train is between, including if it's arriving at a station (currently using two segments before a station as "arriving"); and records that the train's line has a train at that station. After going through all active train positions, the board goes through all stations and sees if any line has a train "at" the station. If a line has a train "at" the station, the LED turns on to that line's color, and turns off if no line has a train there. The board then updates all LEDs to show the new positions, and waits twenty seconds before getting new train positions from WMATA.

***Important:*** Train positions are taken directly from WMATA, and are only as accurate as the location data WMATA provides. In particular, WMATA may report a train's position "at" a station that is closed for repairs, or "at" the station before a series of closed stations long after a train has left. Further, a segment is not a uniform measurement, so while a train may move on the board because it is two circuits away from the station it may not be close enough for an "ARR" message to appear at a station. Finally, the board has LEDs for stations that are not yet open as of April 2023 (i.e. Potomac Yard), and therefore do not turn on. I will try to release software updates as soon as the stations open, but make no guarantees on timeliness. While boards have an auto-update feature, the software is provided as-is and comes with no guarantees or warrantees.

<div style="outline-style: solid; overflow: hidden">
  <h3 style="padding-left: 20px;">Key Open Source Libraries</h3>
    <div class="column">
      <ul>
        <li><a href="https://github.com/esp8266/Arduino">ESP8266 Arduino Core</a></li>
        <li><a href="https://github.com/adafruit/Adafruit_NeoPixel/">Adafruit NeoPixel</a></li>
        <li><a href="https://github.com/tzapu/WiFiManager/">WiFiManager</a></li>
      </ul>
    </div>
    <div class="column">
      <ul>
        <li><a href="https://www.arduino.cc/en/software">Arduino IDE and Main Libraries</a></li>
        <li><a href="https://arduinojson.org/">ArduinoJson</a></li>
      </ul>
    </div>
  </div>