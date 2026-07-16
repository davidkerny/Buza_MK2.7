
FIRMWARE VERSION 6.4.2.4

SETUP:

- Turn off the Crash Detection.
- Turn off the printer model check, firmware version check etc.
- Configure Input Shaper values in the menu: (X:MZV 50Hz, 7:MZV 39Hz..  OR X-Axis: MZV 60 Hz, Y-Axis: MZV 48 Hz, Damping Ratio: 0.1  ??? - NEEDS further testing)
- config for 200step motors only!


TODO on MRS machine: 
- X-axis selftest doesnt pass (axis too long?)

__

Slicer Preset: 
- Import the PrusaSlicer config bundle (File>Import>Import Config Bundle)
- MK3.5 profiles work
- G28 Mesh Bed Levelling


__________________________________________________
HARDWARE:
MK3 or MK2 printer with MINI control board + LCD. 24V PSU and MK52 bed.

Required hardware mods:

- Reverse the Filament sensor logic (preferrably by bypassing the transistor on the IR sensor PCB)
- Change the IR sensor connector with different pinout
- Reverse the X, Y and Z motors movement (In case of X, can be done by physically moving the motor to the front of the X-end part)
- Make a Z motor splitter in order to connect the two Z motors in parallel.
- In case of NOCTUA fan, it spins too slow. Hard wire the fan to 5V (bypassing the PWM) to efficiently cool the extruder heatsink
- Heatbed: change the heatbed connector to be able to connect it. Replace the heatbed fuse to 10-15A.
- Remove the appendix on the Buddy board to flash unsigned firmware
- Some mods are required solely for reverse-compatibility.

Printable parts:

https://www.printables.com/model/65788-buza-mk27-upgrade-for-mk2x
https://www.printables.com/model/65785-buza-mk3b-upgrade-for-mk3s
_________________________________________________________________________________
FW UPDATING: 
Ignore the Firmware Verification Failed message

UPDATING FW PRE-4.4:
First, update to version 4.4 which includes the new bootloader:
https://help.prusa3d.com/downloads/mini-2?versions=all
Only then, flash a newer version.
