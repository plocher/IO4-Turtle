# IO4-Turtle
## License: CERN Open Hardware Licence v1.2

IO4 Tortoise driver with occupancy and point position feedback

Carrier board, DFM, feedback LEDS that don't pass tortoise current and
field changable N/R positioning, feedback and frog selection.


This is an adaptation of my older PIC-based ExpressPCB Turtle
project, which is why the version numbers start at 4….  It has
evolved quite a bit, in form factor and functionality as it has
been used on my layout.

This board mounts on a Tortoise via a sweat-soldered right angle
Molex M-M connector, plugs into an [IOB-Turtle](/pages/IOB-Turtle)
or other IO4 compatible port.

The Tortoise provides:


 * OS section occupancy (so you don't throw a turnout out from under a train...),
 * Turnout point position feedback (Normal, in transit, Diverging)
 * easy frog polarity changes for dealing with wiring mishaps
 * easy Normal/Reverse changes for when the Normal route thru a turnout needs to go the other way.
 * Tortoise motor debouncing when it reaches the end of travel
 * feedback LEDs to show Occupancy (yellow) and commanded position (red/green)


It uses my standard IO4 RJ12/6 wiring interface:


 * pin 1: 9-12vDC
 * pin 2: !DIVERGING - Turnout Position Feedback - low = Diverging, high = not diverging
 * pin 3: !NORMAL    - Turnout Position Feedback - low = Normal, high = not normal
 * pin 4: !OCCUPIED  - Detector Feedback - low = occupied, high = empty
 * pin 5: !MOTOR     - Motor Control Input - Low = Normal, High = Diverging
 * pin 6: GND

It also connects to the local DCC track power feed and to the turnout's isolated-for-detection-purposes stock and frog rails.




