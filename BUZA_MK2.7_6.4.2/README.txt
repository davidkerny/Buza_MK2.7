6.4.2 fw tady - jsou dost zpomaleny rychlosti v ramci debuggingu Crash detection, nakonec byla crash detection vypnuta, tak by to slo zas zrychlit
Zatim krom jedne vytistene kostky netestovano.

Known issues
========================
- Kdyz se da Cancel Print, jede to nahoru extremne pomalu

Positives
========================
- Funguje wifi s ESP
- Funguje Prusa Connect

firmware_MK2.7_6.4.2_fixed_esp.bbf - je pro 200 step motory.

ostatni fw - >??


Input Shaper Settings
=======================
X-axis Filter    MZV
X-axis Freq.     50
Y-axis Filter    MZV
Y-axis Freq.     39


Build Log
=======================
-- Project version: 6.4.2
-- Project version with full suffix: 6.4.2+0.LOCAL
-- Project version with short suffix: 6.4.2+0
-- Using toolchain file: C:/Prusa-Firmware-Buddy-6.4.2/cmake/GccArmNoneEabi.cmake.
-- Bootloader: YES
-- Printer: MINI
-- Board: BUDDY
-- MCU: STM32F407VG
-- Custom Compile Options (C/C++ flags):
-- Web User Interface: YES
-- Connect client: YES
-- Resources: <auto>
-- Option HAS_TRINAMIC: Enabled
-- Option HAS_PAUSE: Enabled
-- Option HAS_CRASH_DETECTION: Enabled
-- Option HAS_POWER_PANIC: Disabled
-- Option HAS_PRECISE_HOMING: Disabled
-- Option HAS_PRECISE_HOMING_COREXY: Disabled
-- Option HAS_PHASE_STEPPING: Disabled
-- Option HAS_PHASE_STEPPING_TOGGLE: Disabled
-- Option HAS_PHASE_STEPPING_SELFTEST: Disabled
-- Option HAS_PHASE_STEPPING_CALIBRATION: Disabled
-- Option HAS_INPUT_SHAPER_CALIBRATION: Disabled
-- Option HAS_SELFTEST: Enabled
-- Option HAS_HUMAN_INTERACTIONS: Enabled
-- Option HAS_LOADCELL: Disabled
-- Option HAS_SHEET_PROFILES: Enabled
-- Option HAS_HEATBREAK_TEMP: Disabled
-- Option HAS_FILAMENT_HEATBREAK_PARAM: Disabled
-- Option HAS_BOWDEN: Enabled
-- Option HAS_MODULAR_BED: Disabled
-- Option HAS_REMOTE_BED: Disabled
-- Option HAS_LOCAL_BED: Enabled
-- Option HAS_PUPPY_MODULARBED: Disabled
-- Option HAS_XBUDDY_EXTENSION: Disabled
-- Option XBUDDY_EXTENSION_VARIANT_STANDARD: Disabled
-- Option HAS_DOOR_SENSOR: Disabled
-- Option HAS_TOOLCHANGER: Disabled
-- Option HAS_SIDE_FSENSOR: Disabled
-- Option HAS_ADC_SIDE_FSENSOR: Disabled
-- Option HAS_FILAMENT_SENSORS_MENU: Disabled
-- Option HAS_ESP_FLASH_TASK: Disabled
-- Option HAS_EMBEDDED_ESP32: Enabled
-- Option HAS_LOVE_BOARD: Disabled
-- Option HAS_TMC_UART: Enabled
-- Option HAS_XLCD: Disabled
-- Option HAS_MMU2: Disabled
-- Option HAS_CONFIG_STORE_WO_BACKEND: Disabled
-- Option HAS_CHAMBER_API: Disabled
-- Option HAS_CHAMBER_FILTRATION_API: Disabled
-- Option XL_ENCLOSURE_SUPPORT: Disabled
-- Option HAS_SWITCHED_FAN_TEST: Disabled
-- Option HAS_HOTEND_TYPE_SUPPORT: Disabled
-- Option HAS_EMERGENCY_STOP: Disabled
-- Option HAS_CEILING_CLEARANCE: Disabled
-- Option HAS_CANCEL_OBJECT: Enabled
-- Option HAS_AUTO_RETRACT: Disabled
-- Option HAS_GCODE_COMPATIBILITY: Disabled
-- Option HAS_UNEVEN_BED_PROMPT: Disabled
-- Option HAS_DOOR_SENSOR_CALIBRATION: Disabled
-- Option HAS_LEDS: Disabled
-- Option HAS_SERIAL_PRINT: Enabled
-- Option HAS_LOCAL_ACCELEROMETER: Disabled
-- Option HAS_REMOTE_ACCELEROMETER: Disabled
-- Option HAS_ATTACHABLE_ACCELEROMETER: Disabled
-- Option HAS_COLDPULL: Disabled
-- Option HAS_BED_LEVEL_CORRECTION: Enabled
-- Option HAS_SHEET_SUPPORT: Enabled
-- Option HAS_NFC: Disabled
-- Option HAS_NOZZLE_CLEANER: Disabled
-- Option HAS_BELT_TUNING: Disabled
-- Option HAS_MANUAL_BELT_TUNING: Disabled
-- Option HAS_I2C_EXPANDER: Disabled
-- Option HAS_WASTEBIN: Disabled
-- Option HAS_PRINT_FAN_TYPE: Disabled
-- Option HAS_GEARBOX_ALIGNMENT: Disabled
-- Option HAS_CHAMBER_VENTS: Disabled
-- Option TRANSLATIONS_IN_EXTFLASH: Enabled
-- Option HAS_TRANSLATIONS: Enabled
-- Option ENABLE_TRANSLATION_CS: Disabled
-- Option ENABLE_TRANSLATION_DE: Disabled
-- Option ENABLE_TRANSLATION_ES: Disabled
-- Option ENABLE_TRANSLATION_FR: Disabled
-- Option ENABLE_TRANSLATION_IT: Disabled
-- Option ENABLE_TRANSLATION_JA: Disabled
-- Option ENABLE_TRANSLATION_PL: Disabled
-- Option ENABLE_TRANSLATION_UK: Disabled
-- Option HAS_TOUCH: Disabled
-- Option RESOURCES: Enabled
-- RESOLUTION: W240H320
-- Graphical User Interface: YES
-- Option HAS_GUI: Enabled
-- Option HAS_PLANNER: Enabled
-- Option HAS_BURST_STEPPING: Disabled
-- Option HAS_LOADCELL_HX717: Disabled
-- Option HAS_ADVANCED_POWER: Disabled
-- Option HAS_ACCELEROMETER: Disabled
-- XLCD_TOUCH_DRIVER: NO
-- Option HAS_DWARF: Disabled
-- Option HAS_PUPPIES: Disabled
-- Option HAS_USB_DEVICE: Enabled
-- Option HAS_MMU2_OVER_UART: Disabled
-- Option HAS_PUPPIES_BOOTLOADER: Disabled
-- Option PUPPY_FLASH_FW: Disabled
-- Option HAS_SIDE_LEDS: Disabled
-- Option HAS_LEDS_MENU: Disabled
-- Option BOOTLOADER_UPDATE: Enabled
-- Option NETWORKING_BENCHMARK_ENABLED: Disabled
-- Option HEAP_INSTRUMENTATION_ENABLED: Disabled
-- Option DEVELOPER_MODE: Disabled
-- Option DEBUG_WITH_BEEPS: Disabled
-- Option WEBSOCKET: Enabled
-- Option MDNS: Enabled
-- Configured to generate .bbf version of the firmware.
-- Signing Key:
-- Configuring done (7.5s)