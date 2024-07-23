# pscards
Custom cards for restoring or repairing Korg PS-3x00 polyphonic synthesizers

## Overview

### Goal
Korg Polyphonic Synthesizers (PS-3100, PS-3200, PS-3300) are complex and expensive synthesizers, but as these instruments are now at least 45 years old, occasionally their original parts fail, and there is a need for recreated parts, in order to keep the instrument in operating condition.

This project is to create spare circuit boards to keep these old synthesizers operating.


### Sub-Projects
- [`KLM-69`](KLM-69) : KiCad project
	-	KLM - 69 "GATE" board
		-	PS-3100 has KLM-69E
		-	PS-3200 has KLMC-69F or KLM-69G  (are these identical, unknown revision?)
- [`KLM-64`](KLM-64) : KiCad project
	-	KLM - 64 "SIGNAL GENERATOR" board
		-	PS-3100 has KLM-64E
		-	PS-3200 has KLMC-064D  (are these identical, unknown revision?)
- [`card-extender`](card-extender) : KiCad project
	-	Diagnostic support board
		-	A pass-through board that extends a card outside the Korg synth chassis, to enable easier access while diagnosing and repairing
		-	Plugs-in to Korg synth backplane, and provides 2 44-pin card socket connections to host the Korg KLM board.
		-	Sockets can be: [Sullins EBM22DREH](https://www.sullinscorp.com/product/?pn=EBM22DREH), [EDAC 305-044-520-202](https://edac.net/series/305?search_part=305-044-520-202), [Vector R644](https://www.vectorelect.com/connector-card-edge.html) or similar card sockets.
		-	Provides test-points in Molex 0.156” (3.96mm) header format, using vertical headers, [Molex KK396 part #0026481240](https://www.molex.com/en-us/products/part-detail/26481240)
- [`klib`](klib) : “KiCad Libraries” folder
	-	KiCad shared libraries (symbols, footprints, images, drawing sheets, project templates, 3D models) to be used common across sub-projects
	-	Shared folder should be referenced in sub-projects as `${KIPRJMOD}/../klib/`


## Criteria

### Technical Requirements
Original boards are:
- single-sided:
  - top layer has silk-screen component labels but no traces or soldermask
  - bottom layer of board has copper traces and soldermask
- 1.6mm thickness PCB
- 1oz. copper plating
	
#### Dimensions
- Dimensioning of card assumes landscape orientation
- Height: 177mm  (including edge-connector).
- Width: 240mm
- Edge connector pads mirror card-edge traces, but there can be some variance in edge connector sizing & placing
	- Edge connectors can be between 87.5mm & 89mm in width and 10mm in height.
	- Edge connectors can be from 14mm to 15.5mm from outer (left/right) card edge.
	- Edge connectors can have a 32.5mm to 34mm gap between them.



### Design Requirements
- Circuit projects require KiCad 8.0+
- Schematics pages are A4-sized
- Dimensioning in millimeters (mm)


## Notes

### External Resources
- Korg PS-3100 Schematic PDF document was retrieved from: https://archive.org/details/synthmanual-korg-ps-3100-schematics/

### Original Work is by Korg
- All references to the word Korg, pcb names and numbers, (KLM*) or use of Korg component references or other design, are based on the original work by Korg.
- This work in this project is to repair and restore an original Korg synthesizer, based on its service documents and schematics.

