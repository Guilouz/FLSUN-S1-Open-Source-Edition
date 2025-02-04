---
icon: material/clipboard-list
hide:
  - toc
---

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
