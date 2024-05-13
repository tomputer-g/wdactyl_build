## What?

This repo keeps track of all necessary steps and files relating to the Dactyl Manuform build I performed in May 2024. 

## Resources and links

Inspiration from https://www.youtube.com/watch?v=95etDQ0I-Ls (Building a Custom Split Ergonomic Keyboard with a Trackpoint - wDactyl). 

In turn the youtuber provided links to his repository here: https://github.com/JanLunge/keyboards/tree/main/wDactyl%20-%20large, https://github.com/JanLunge/keyboards/tree/main/keycaps, and https://github.com/JanLunge/vial-qmk/tree/vial/keyboards/janlunge/wdactyl (TODO not used so far, but contains keymapping).

## Hardware

Keys: Gateron Yellow 3rd gen linear ($30 ish from Amazon) x74

Keycaps and case were 3D printed based on the links above.

Arduino Pro Micro x2 from existing stock

TODO TRRS linking.

Soldering is done by hand without any fancy PCBs (just row wise diodes and column wise wires).

Left hand side: Top-down: A2, A1, A0, 15, 14, 16, 10; thumb-cluster to other side: 9, 8, 7, 6, 5, 4

RHS not done yet.

## Software

TODO adopt JanLunge's keymapping as well as firmware.

Commands done so far on my own (using QMK MSYS and QMK Toolbox):

```
qmk setup
qmk config user.keyboard=handwired/dactyl_manuform/6x6/promicro 
qmk import-keymap <path-to-layout>/layout.json
qmk flash -kb handwired/dactyl_manuform/6x6/promicro -km handwired_dactyl_manuform_6x6_promicro_layout_6x6_mine
```
This layout gave me 36 out of 37 keys, not sure what was missing.

## What next?

* Explore 'official' keymapping from JanLunge.
* Finish RHS wiring and connect both halves
* See if I need actually nicer keycaps