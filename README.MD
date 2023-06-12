The simplest possible mains PSU
I needed one for the used Tektronix active probe (p6201) I bought off ebay.

The PSU take 120V mains and outputs +/- 15V, 175mA max (each rail)
I added varistor, 250mA fuse on the input and 15V zeners on the output.

If one tries to draw more current, the mains ripple appears on the output.

See LTSpice folder for the sim files.
See Kicad folder for schematic/pcb layout

Interesting bits:

* It is a full wave voltage dubler PSU. https://sound-au.com/project05-mini.htm
This is rather unfortunate, but the transformer I salvaged only had ~17VAC, this is not enough for the more conventional type with a full wave bridge rectifier. The price is much larger input caps and extra heat that is burned when voltage is regulated down to +/- 15V.

* Two LEDs are here to signal that both rails are healthy and bleed off these large resistors. If a regulator shutdowns (over current, overheating) corresponding LED goes off.

* Large, 2W 3 Ohm resistors are there to burn heat, and reduce the heat dissipation requirments for the voltage regulator. I did not have smaller, 2W rated, ones. If I did - the PSU could either use smaller caps, or product larger output current.

* Since this is not a switching PSU, not extra filtering is needed. Not backfeed filtering is needed either.

* I use aluminum enclosure as a heat sink. Regulators are connected by wires to the PCB and screwed right to the aluminum.

* For the enclosure - I saw a large salvaged box one in halfs, 3d printed a PETG cap where IEC AC socket and AC main switch are mounted.