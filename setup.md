---
title: Setup Your Board
description: >-
  Getting started with your DCTransistor board
---


# Setup Instructions
To get your board to work, you only need to provide it with power and WiFi information. 

In short:
1. Plug your board into a 5V wall / phone charger, or a computer, with a USB-C cable
2. Join the `DCTransistor` WiFi network and follow the WiFi setup prompts

### Power
Boards can be powered with a USB-C cable **or** a battery with a JST-PH 2.0 connector. Either power source must provide 5 volts (5V) of power - providing more volts may damage your board, and fewer may cause LEDs to dim or blink out.

<figure style="text-algin: center">
<img src="/images/initial_power.jpg" style="height: 300px; width: 300px;">
<img src="/images/usb_and_battery_power.jpg" style="height: 300px; width: 300px;">
<img src="/images/battery_power.jpg" style="height: 300px; width: 300px;">
<figcaption>Above: Board powered with USB cable, board powered with a USB cable and battery pack, and board powered with just a battery pack.</figcaption>
</figure>

The simplest power source is a USB-C cable attached to a phone charger or computer. Be sure to check your power supply, but most chargers will provide 5V.

Alternatively, you can use a battery or alternative power supply that provides approximately 5V of power through a JST-PH 2.0 connection. For example, a [3x AA battery holder](https://www.adafruit.com/product/4779) will provide sufficient power with three fully charged batteries.
**Caution**: Batteries may drain quickly when powering the board alone. For continuous use, a stable power supply is recommended.

You may also power your board using both the USB-C and JST connections. Doing so should draw less power from both supplies.

### WiFi

<div style="float: left; margin: 15px; width: 330px;">
  <figure>
    <img src="/images/choose_wifi_network.jpg">
    <figcaption>1. In your device WiFi settings, connect to the new DCTransistor network</figcaption>
  </figure>
  <figure>
    <img src="/images/redirection.jpg">
    <figcaption>2. Redirection after connecting</figcaption>
  </figure>
</div>

#### Short Instructions
The first time you turn your board on or change WiFi networks:
1. Connect to the `DCTransistor` WiFi with password `trainsareneat`.
2. On the WiFi landing page (or at `192.168.4.1` in a web browser), select your WiFi and enter your WiFi password.
3. Wait for the board to [update](#troubleshooting)

#### Detailed Instructions

The first time you plug in your DCTransistor board, it will create a new WiFi network named `DCTransistor` with a password `trainsareneat`.

When you join the WiFi network, you should be automatically redirected to a menu option to select a WiFi network for the board to join. If you are not redirected, go to `http://192.168.4.1` in a web browser. 

After setup, the board will automatically connect to your network every time it turns on. If it is unable to connect to your network, it will recreate the DCTransistor network and wait for you to select a new one to join.

<div style="text-align: center">
<figure style="width: 300px; display: inline-block; vertical-align: top">
  <img src="/images/selection_screen.jpg">
  <figcaption>3. Choose "Configure Wifi"</figcaption>
</figure>
<figure style="width: 300px; display: inline-block; vertical-align: top">
  <img src="/images/wifi_info_entered.jpg">
  <figcaption>4. Select your WiFi network from the networks listed and enter your network password</figcaption>
</figure>
</div>

<div style="float: left; margin: 5px; width: 330px;">
  <figure>
  <img src="/images/connecting_waiting.jpg">
  <figcaption>5. Your board will try to connect to your network</figcaption>
  </figure>
  <figure>
  <img src="/images/initial_install.jpg">
  <figcaption>6. After connecting, your board will download the latest DCTransistor software and the WiFi light turns blue</figcaption>
  </figure>
</div>

While it is waiting for you to connect it to your Wifi, or while it is connecting to your WiFi as it turns on, the board's WiFi status LED will remain yellow.

### Updates
The board checks for software updates every time it turns on, and will automatically update itself if there is a newer version of software.

When the board is updating, the WiFi status LED will turn blue. When it is done updating, the board restarts, the WiFi and Web status LEDs turn off, and it connects to WiFi and the Web the same as if it just turned on.


### Troubleshooting
Though the board shouldn't have any problems that aren't quickly addressed through an update, it is possible that something may prevent your board from automatically updating itself or that an issue with the boards goes unnoticed.

If this happens, first manually install the most recent software version using the instructions under [customize your board](#customize-your-board).

If the problem persists with the latest software version, send an email to <a href="mailto:support@dctransistor.com">support@dctransistor.com</a> or create an issue on [GitHub](https://github.com/LArkema/dctransistor-project/issues)

<figure>
  <img src="/images/setup_complete.jpg">
  <figcaption style="text-align: center">7. After donwloading, the board resets and begins showing train locations</figcaption>
</figure>