# Belak's Ender 3v2 Klipper Setup

## Hardware

- Ender 3v2
- SKR Mini E3v3
- Stock hotend
- Sherpa Mini extruder
- [Manta MK2](https://www.printables.com/model/169137-manta-mk2-duct-tool-head-system) toolhead (with dual 5015 fans)

## Sources

- Default [SKR Mini E3v3](https://github.com/Klipper3d/klipper/blob/master/config/generic-bigtreetech-skr-mini-e3-v3.0.cfg) config
- Default [Ender 3v2](https://github.com/Klipper3d/klipper/blob/master/config/printer-creality-ender3-v2-2020.cfg) config
- [Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder/blob/master/Klipper_Config_Block.txt) config tweaks

## Macros

This also includes a number of macros, primarily modified from users in the Prusa3D discord.

- `CG28` - issue a `G28` if not already homed
- `LOAD_FILAMENT` - convenience macro for preheating and loading filament, from Discord
- `UNLOAD_FILAMENT` - convenience macro for preheating and unloading filament, from Discord

These macros are hidden because they're really only needed for gcode files.

- `_START_PRINT` - preheat bed and extruder, home the bed, set up a mesh using KAMP, purge filament
- `_END_PRINT` - turn everything off and move up a few mm

## Setup

While most things should work out of the box, this config assumes the following are cloned somewhere and symlinked into the `printer_data/config` directory.

- [KAMP](https://github.com/kyleisah/Klipper-Adaptive-Meshing-Purging)
- [mainsail-config](https://github.com/mainsail-crew/mainsail-config)
- [moonraker-timelapse](https://github.com/mainsail-crew/moonraker-timelapse)
