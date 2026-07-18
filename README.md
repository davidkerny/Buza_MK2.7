# Buza MK2.7 Upgrade

An upgrade project enabling you to run Prusa MINI's Buddy board control electronics on older MK2/MK3 frames.

---

## 🚀 Quick Start: How to Start Printing

1. **Download** the latest [PrusaSlicer Config Bundle (.ini)].
2. In PrusaSlicer, navigate to:
   > **File** > **Import** > **Import Config Bundle**
3. Select the downloaded `.ini` file and confirm.
4. Slice and Print some fancy stuff.

---

## ⚙️ Slicer Presets Details

* **PrusaSlicer profiles and settings:** Download and import the Config Bundle via `File > Import > Import Config Bundle`.
* **Profiles:** Standard **MK3.5 profiles** also work out of the box. The printer eats the MK4 and MINI Gcodes too.
* **Homing & Levelling:** Utilizes `G28` for **Mesh Bed Leveling** (MK3S uses G80)

---

## 🔧 Printer Setup & Configuration

Once flashed, ensure the following settings are configured in the printer menu:

* **Recommended: Disable Protections:**
    * Turn **OFF** Crash Detection.
    * Turn **OFF** the G-code checks. (Settings>Hardware>G-Code Checks)
* **Motors:**
    * FW 6.6.0.3 includes versions for **200-step (default) as well as 400-step motors**
* **Input Shaper Tuning** *(Under Active Testing)*:
    * *Option A:* **X-Axis:** `MZV 50Hz` | **Y-Axis:** `MZV 39Hz` (Works on AER Machines)
    * *Option B:* **X-Axis:** `MZV 60Hz` | **Y-Axis:** `MZV 48Hz` (Damping Ratio: `0.1`, AI suggestion for MK3.5 ???)
    * *Note: Input Shaper values might still need further verification.*

---

## 🔌 Hardware Requirements & Modifications

### Core Requirements:
* **Frame/Bed:** Prusa MK3 or MK2 printer frame with a **24V PSU** and **MK52 heated bed**.
* **Electronics:** Prusa **MINI Buddy control board** + **MINI LCD**.

### Required Hardware Mods to Build a New MK2.7:

[ Buddy Board ] ──> Remove Appendix (Allow Unsigned FW)
│
├──> [ Filament Sensor ] ──> Reverse Logic (Bypass IR PCB Transistor) & Change Pinout
├──> [ X, Y, Z Motors ]  ──> Reverse Direction (X can be flipped physically to the front)
├──> [ Z Motors ]        ──> Parallel Splitter Cable (Connect both Z-motors to 1 port)
├──> [ Noctua Fan ]      ──> Hardwire to 5V (Bypassing PWM for adequate cooling)
└──> [ Heatbed ]         ──> Swap connector & upgrade fuse to 10-15A


* **Buddy Board:** Physical removal of the appendix/breakaway tab on the Buddy board is required to flash unsigned/custom firmware.
* **Filament Sensor:** Reverse the IR sensor logic (preferable by bypassing the transistor on the sensor PCB) and modify the connector pinout.
* **Motors Direction:** Reverse X, Y, and Z stepper directions.
    * *Tip:* For the X-axis, this can be alternatively solved by physically mounting the motor to the front of the X-end part.
* **Z-Axis:** A custom parallel splitter cable is required to connect both Z-axis stepper motors to the single Z-port on the Buddy board.
* **Hotend Fan (Noctua):** The standard Noctua fan spins too slowly under PWM control on this board. **Hardwire the fan directly to 5V** (bypassing PWM) to ensure sufficient extruder heatsink cooling.
* **Heatbed:** Modify the heatbed connector for Buddy board compatibility. **Replace the heatbed fuse with a 10-15A rated fuse.**
* *Note: Some modifications are required solely for firmware reverse-compatibility with the existing MK2.7 printers.*

---

## 📐 Printable Parts

Get the printed parts designed specifically for these builds:

* [Buza MK2.7 Upgrade for MK2.x](https://www.printables.com/model/65788-buza-mk27-upgrade-for-mk2x) (on Printables)
* [Buza MK3b Upgrade for MK3S](https://www.printables.com/model/65785-buza-mk3b-upgrade-for-mk3s) (on Printables)


---

### Upgrading from older Firmware (Pre-4.4):
If your board is running firmware older than `4.4`, you must perform a step-by-step upgrade in order to upgrade the ancient bootloader:
1. First, flash **version 4.4** (with bootloader 2.0): [Prusa MINI Firmware Downloads](https://help.prusa3d.com/downloads/mini-2?versions=all).
2. Only after a successful update to `4.4` can you flash the newer firmware versions (6.x+).

