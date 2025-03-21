---
icon: material/file-restore
hide:
  - toc
---

The Open Source OS is already ready to use and configured for the FLSUN S1 Stock version but make sure to always use the latest available Klipper configuration files after installation.

<br />

- To update to latest Klipper configuration files and configure your printer, connect to printer over SSH (see <a href="../ssh-connection">:material-console: SSH Connection</a> section).

- In the SSH command prompt window, enter the following command to start **Easy Installer**:

	``` title="SSH Command Prompt"
	easy-installer
	```

	<img width="900" src="../assets/images/installer-01.png">

- Enter ++"3"++ for **Extras** menu → ++"1"++ for **Update Klipper configuration files** → ++"Enter"++ to confirm your choice:

	<img width="900" src="../assets/images/installer-04.png">

- Confirm your choice with ++"Y"++ then ++"Enter"++ and configuration files will be downloaded:

	<img width="900" src="../assets/images/installer-05.png">

- And configure features you need:

    <img width="900" src="../assets/images/installer-06.png">

- After that, **don't forget to calibrate your printer before starting a print!**:

    Go to the **`Configurations`** → **`Calibrations`** menu.
    
    - **Motors Calibration** → To calibrate Motors
    - **Z Offset Calibration** → To calibrate Z Offset
    - **Bed Mesh** → To perform Delta Calibration and Bed Leveling
    - **Input Shaper** → To measure Resonances

- Also make sure you always use the latest version of **Moonraker**, **Klipper** and **KlipperScreen** available via **Mainsail** or **Fluidd**'s Update Manager.

- Enjoy :smiley:

!!! Note
    The installer downloads the latest version of Klipper configuration files but if needed, they are available <a href="https://github.com/Guilouz/Klipper-Flsun-S1/tree/master/config/FLSUN%20S1">here</a>.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
