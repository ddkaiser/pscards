# pscards
Custom cards for restoring or repairing Korg PS-3x00 polyphonic synthesizers

## Overview

### Goal
Korg Polyphonic Synthesizers (PS-3100, PS-3200, PS-3300) are complex and expensive synthesizers, but as these instruments are now at least 45 years old, occasionally their original parts fail, and there is a need for recreated parts, in order to keep the instrument in operating condition.

This project is to create spare circuit boards to keep these old synthesizers operating.


### Sub-Projects
- `KLM-69` : KiCad project
	-	KLM - 69 "GATE" board
		-	PS-3100 has KLM-69E
		-	PS-3200 has KLMC-69F or KLM-69G  (are these identical, unknown revision?)
- `KLM-64` : KiCad project
	-	KLM - 64 "SIGNAL GENERATOR" board
		-	PS-3100 has KLM-64E
		-	PS-3200 has KLMC-064D  (are these identical, unknown revision?)
- `klib` : “KiCad Libraries” folder
	-	KiCad shared libraries (symbols, footprints, images, sheet templates) to be used common across sub-projects
	-	Referencable in sub-projects as `${KIPRJMOD}/../klib/`


## Criteria

### Technical Requirements
Original boards are:
- single-sided:
  - bottom of board has copper traces and soldermask
  - top layer has silk-screen component labels but no traces or soldermask
- ?mm thickness
- ?oz copper plating

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

