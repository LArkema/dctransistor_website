---
title: How it Works
description: >-
  Details about how the board updates its display
---

<img class="cover-board" src="{{ site.baseurl }}/images/lightup-board.jpg" alt="Large picture of a DCTransistor board, powered on to show live train positions. The board is programmable circuit board, mostly light green except for a dark green title and dark green rectangles representing the DC metro train lines, a beige boundary representing the beltway, and silver representing the Potomac and Anacostia rivers. It is designed to represent the DC Metro System map.">

Boards work by getting real-time train positions WMATA makes available through it's [API](https://developer.wmata.com/docs/services/5763fa6ff91823096cac1057/operations/5763fb35f91823096cac1058), and turning on LEDs for the station a train is arriving at or has most recently left from. 

When the board turns on, it turns all LEDs off except the power LED (some other LEDs may flash on with instructions from before the board turned off), then attempts to connect WiFi. At this point, the WiFi LED will turn yellow until it successfully connects (which may take a few seconds), and then it will turn green. The board then attempts to connect to the WMATA API, and the Web LED will turn yellow until it successfully receives the first batch of train positions.

WMATA provides a list of every train in service, the line it's on, and which circuit (i.e. track segment) it's currently on. For each train, the board checks which stations the train is between, including if it's arriving at a station (currently using two circuits before a station as "arriving"); and records that the train's line has a train at that station. After going through all active train positions, the board goes through all stations and sees if any line has a train "at" each station, setting the LED for that station to the line's color if there is and turning the LED off if not. The board then updates all LEDs to show the new positions, and waits twenty seconds before getting new train positions from WMATA.

***Important:*** Train positions are taken directly from WMATA, and are only as accurate as the location data WMATA provides. In particular, WMATA may report a train's position "at" a station that is closed for repairs, or "at" the station before a series of closed stations long after a train has left. Further, a circuit is not a uniform measurement, so while a train may move on the board because it is two circuits away from the station it may not be close enough for an "ARR" message to appear at a station. Finally, the board has LEDs for stations that are not yet open as of July 2022 (i.e. Potomac Yard and the Silver Line Expansion), and therefore do not turn on. I will try to release software updates as soon as the stations open, but make no guarantees on timeliness. You are responsible for updating your board with any new software, though I will try to maintain voluntary notification emails.

### Old Boards
The current version of the board got here through prototyping and trial and error. If you're interested in prior versions of the board, or have one you want to update, see [Old Boards](/old-boards)