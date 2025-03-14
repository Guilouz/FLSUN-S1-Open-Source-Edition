---
icon: material/clipboard-list
hide:
  - toc
---

## FLSUN OS - 1.4 (Public Release)
<hr>

- Added in-image security with bootloader core board: In case the eMMC is corrupted or unbootable, booting via microSD is still possible.
- Now possible to install **FLSUN OS** on eMMC. See <a href="../install-flsun-os-on-emmc">:octicons-cpu-16: Install FLSUN OS on eMMC</a> section.
- Added possibility to Unload Filament with Purge or Retraction with new macros. **KlipperScreen** has also been updated for this.

    <img width="600" src="../assets/images/screenshot_05.png">


You can update configuration files with **`easy-installer`** command in SSH but for more security it's necessary to install this new image.


## FLSUN OS - 1.3 (Public Release)
<hr>

- The system is now shutdown properly when the printer is powered off.
- Reworked Power Loss Recovery. It now resumes exactly where it left off and it also preserves all settings like filament used, chamber fan speed, extrude mode, speed factor, extrude factor and all velocity parameters. **Klipper** has also been updated for this.
- Improved Bed Mesh with `zero_reference_position` parameter.
- Added support for Chamber LED brightness control in **KlipperScreen**.
- Macros now respect current configuration settings.
- Improved Gcode Offsets to apply them to Endstops. **KlipperScreen** has also been updated for this.
- Improved Bed Mesh with `zero_reference_position` parameter.
- Improved `SET_GCODE_OFFSET` macro.
- Improved `RESUME` macro: Shutdown fan for heating.
- Set default PID Hotend Calibration temperature to reasonable 250°C.
- Changes default extruder curent to 0.8.
- Updated **KlipperScreen** environment.

You can update configuration files for fixes with **`easy-installer`** command in SSH. Environment is updated automatically when **KlipperScreen** is updated with Update Manager.


## FLSUN OS - 1.2.2 (Public Release)
<hr>

- Fixed issue with error message `dict object has no attribute max_power` when resuming.

You can update configuration files for fixes with **`easy-installer`** command in SSH.


## FLSUN OS - 1.2.1 (Public Release)
<hr>

- Fixed issue with error message `This macro cannot be used while printing!`.
- `SET_TMC_CURRENT` command now integrated in macros. It's no longer necessary to add it in the slicer Start Gcode.

You can update configuration files for fixes with **`easy-installer`** command in SSH.


## FLSUN OS - 1.2 (Public Release)
<hr>

- Added **Easy Installer** to facilitate installations and some actions with the simple **`easy-installer`** command in SSH:
    - Install/Update/Remove **Spoolman** (Filament Spools Management).
    - Install/Remove **GuppyFLO** (Remote Access via TCP Proxy).
    - Backup/Restore **Klipper** configuration files.
    - Backup/Restore **Moonraker** database.
    - Delete cache and logs files.
    - Update **Debian** packages.
    - Restore Web-UI default settings.
    - Restore SSH access for Stock OS.
- Added support for Numpy.
- Added possibility to generate resonances graphics with `GENERATE_RESONANCES_GRAPHICS` macro.
- Added support for **BigTreeTech MMB Cubic** to add chamber temperature sensor and Neopixels.
- Added support to choose Bed Mesh type before printing. You can now choose type of bed mesh you want to start before printing (Full Bed Mesh, Adaptive Bed Mesh or No Mesh).
- Added possibility to take screenshots of **KlipperScreen** with `_SCREENSHOT` command (screenshots are saved in config folder).
- Improved **Delta Calibration** function with new enhanced method. More accurate and with denser coverage that allows better detection of variations of the bed or in the mechanics of the printer, which can improve print quality. You can revert back to classic method by changing `enhanced_method` parameter to **`False`** (in `[delta_calibrate]` function of `printer.cfg` file).
- Updated **KlipperScreen** service file to wait for Moonraker if present, to not fail the connection on startup and having to retry.
- Updated Virtual Environments.
- Updated `.kiauh.ini` file to allow to use the new **Kiauh** version.
- **Kiauh** can now be started with the simple **`kiauh`** command in SSH.
- Updated **Klipper** configuration files.
- Integrated latest Moonraker, Klipper, KlipperScreen, Mainsail and Kiauh builds.


## FLSUN OS - 1.1 (Beta Release)
<hr>

- Updated kernel to restore CPU frequency to 1.5GHz instead of 1GHz (50% increase in performance).
- Disabled Wi-Fi Power Management, this frees up bandwidth, and increases camera fps.
- Integration of **GuppyFLO**, a lightweight self-hosted service that allows remote management via TCP Proxy using Moonraker and Tailscale.
- Replaced hostname `FLSUN-OS-XXXX` with `FLSUN-S1-XXXX` (still based on MAC address).
- Improved SSH header.
- Updated **Klipper** configuration files.
- Updated Web interface configuration files.
- Integration of FLSUN Gcodes files.
- Fixed screen brightness.


## FLSUN OS - 1.0 (Beta Release)
<hr>

- Initial Beta Release

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
