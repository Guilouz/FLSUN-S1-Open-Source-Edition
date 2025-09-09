---
icon: material/information-variant-circle
hide:
  - toc
---

<img width="700" src="../assets/images/home.png">

**FLSUN-OS** is an Open Source version for **FLSUN S1** and **FLSUN S1 Pro** that uses the microSD port of the core board to boot on a new OS.

This means that the Stock OS is not modified. It’s a kind of dual boot, it's easy to go back to Stock OS but it can also be installed on eMMC memory.

This new OS is based on :simple-debian: ***Debian 13 Trixie*** and is ready to use. It's more stable and has better performance.<br />
It has the advantage of having a support until June 2030 unlike Debian 10 (Stock OS) which expired in June 2024.

Benchmark comparison between **STOCK OS** (Board flsun) and **Open Source Edition OS** based on Debian 12 (FLSUN-OS): <a href="https://browser.geekbench.com/v5/cpu/compare/22823940?baseline=22823878">:material-web: Geekbench.com</a>

**What's included:**

  - Upgraded kernel a little faster and which gives access to the 1 GB of RAM (700 MB on Stock OS)<br />
  - Enabled ZRAM swap to add extra 512 MB of RAM<br />
  - SSH access<br />
  - Moonraker (latest build)<br />
  - Klipper (latest build with modifications for S1 support, repo is available <a href="https://github.com/Guilouz/Klipper-Flsun-S1">:material-github: here</a>)<br />
  - KlipperScreen (latest build with modifications for S1 support, repo is available <a href="https://github.com/Guilouz/KlipperScreen-Flsun-S1">:material-github: here</a>)<br />
  - Mainsail (latest build)<br />
  - MJPG-Streamer (latest build)<br />
  - Kiauh (latest build)<br />
  - Pre-configured Web interfaces for Mainsail and Fluidd<br />
  - Improved Klipper configuration files (M600 support, Drying Box from Web interfaces support, etc...)<br />
  - Improved Power Loss Recovery<br />
  - Easy Installer feature to facilitate programs installation and some actions<br />
  - Enhanced Delta Calibration feature (more accurate and better detection of variations of the bed or in the mechanics of the printer, which can improve print quality)<br />
  - Bed Mesh Type before printing feature (Full Bed Mesh, Adaptive Bed Mesh or No Mesh)<br />
  - Adaptive Bed Heating feature (heated bed area depending on the model size)<br />
  - Moonraker Timelapse support<br />
  - Klipper Print Time Estimator support <br />
  - BigTreeTech MMB Cubic support (Chamber Temperature Sensor and Neopixels)<br />
  - BigTreeTech Smart Filament Sensor V2.0 support<br />

!!! Note
    All AI features have been removed as they do not work as expected.<br />Only Power Loss Recovery and XY Dimension Calibration features have been kept.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
