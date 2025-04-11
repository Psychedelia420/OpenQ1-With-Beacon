# OpenQ1 - With Becon
The goal of this project is to create custom, community supported firmware for the QIDI Q1 Pro 3D printer, including:
- All features of the stock firmware, excluding PLR and the orignal probe (this repo adds the use of a beacon probe using the mount [here](https://github.com/keyboardspecialist/q1pro_beacon/blob/main/beacon%20shroud%20v11.step))
- The latest versions of klipper, moonraker, fluidd, etc
- Latest version of Debian & Linux LTS for improved security 
- Improved configuration and macros

## Features:
- Latest version of Debian (Bookworm currently)
- Latest LTS Linux Kernel (6.6.x currently)
- Printer software pre-installed:
    - Klipper
    - Moonraker
    - Fluidd
    - Crowsnest
    - moonraker-timelapse
- Improved Q1 Pro klipper config and Stock Macros with the beacon changes
- Changes Already made to run the beacon probe on the firmware, also reverted to stock macros and modified them for the probe to improve the wiping process of the nozzle over the Original OpenQ1 branch.
- All stock features of the Q1 Pro, except
    - [QIDI Auto Z Offset](https://github.com/frap129/qidi_auto_z_offset)
    - Shake&Tune
    - Power loss recovery was hacky at best on the stock fimrware, and is not included.
    - [Screen support](https://github.com/frap129/klipmi) is still a WIP and is not included by default.

# How to install:
Follow the [installation guide](docs/Installation.md). Note that this is still in testing, bugs are to be expected. Please report issues and feature requests in this repo.

### Calibrate Z Offset
Automatically done by running `BEACON_AUTO_CALIBRATE` Instead of having to manually set Z offset; Ignore the save changes & restart after the first initial auto calibrate until i figure out how to solve this...

### Change Slicer Settings
OpenQ1 makes some changes to the `PRINT_START` and `PRINT_END` macros that don't always behave well with the default slicer settings. It is recommended that you change them, following the guide here: [Slicer Setup](docs/Slicer-Setup.md).
