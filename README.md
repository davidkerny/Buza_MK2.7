
FIRMWARE VERSION 6.4.2

- Turn off the Crash Detection.
- Configure Input Shaper values in the menu: (X-Axis: MZV type at 60 HzY-Axis: MZV type at 48 HzDamping Ratio: 0.1  ??? - NEEDS TESTING)
- for 200step motors only


MRS machine specifics: 
- ESP WiFi doesnt work for some reason ?!?
- X-axis selftest doesnt pass (axis too long?)

__

Slicer Preset: 
- Import the PrusaSlicer config bundle (File>Import>Import Config Bundle)
- MK3.5 profiles work
- G28 Mesh Bed Levelling


__________________________________________________
HARDWARE:
MK3 printer with MINI control board + LCD
Eventually built on MK2 frame with 24V PSU and bed
Required hardware mods:
- Reverse the Filament sensor logic (preferrably by bypassing the transistor on the IR sensor PCB)
- Change the IR sensor connector with different pinout
- Reverse the X, Y and Z motors movement (In case of X, can be done by physically moving the motor to the front of the X-end part)
- Make a Z motor splitter in order to connect the two Z motors in parallel.
- In case of NOCTUA fan, hard wire the fan to 5V (bypassing the PWM) to efficiently cool the extruder heatsink
- Heatbed: change the heatbed connector to be able to connect it. Replace the heatbed fuse to 10-15A.
- Remove the appendix on the Buddy board to flash unsigned firmware
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
