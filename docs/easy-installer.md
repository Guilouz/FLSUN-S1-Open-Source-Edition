---
icon: material/star
hide:
  - toc
---

**Easy Installer** allows you to install programs or perform some actions in an easy way.

- To run it, connect to printer over SSH (see <a href="../ssh-connection">:material-console: SSH Connection</a> section).

- In the SSH command prompt window, enter the following command to start **Easy Installer**:

	``` title="SSH Command Prompt"
	easy-installer
	```

	<img width="900" src="../assets/images/installer-01.png">


	### Install Menu
	
	<img width="900" src="../assets/images/installer-02.png">


	- **1) Install or Update Spoolman** → See <a href="../spoolman/#install-spoolman">:material-circle-double: Spoolman</a>
	- **2) Install GuppyFLO** → See <a href="../remote-access/#install-guppyflo">:material-earth: Remote Access</a>


	### Remove Menu

	<img width="900" src="../assets/images/installer-03.png">


	- **1) Remove Spoolman** → See <a href="../spoolman/#remove-spoolman">:material-circle-double: Spoolman</a>
	- **2) Remove GuppyFLO** → See <a href="../remote-access/#remove-guppyflo">:material-earth: Remote Access</a>


	### Update Menu

	<img width="900" src="../assets/images/installer-04.png">


	- **1) Update Klipper configuration files** → This allows to update your printer with latest Klipper configuration files
	- **2) Printer Setup Wizard** → This helps you to configure your printer with the desired features
	- **3) Update Motherboard MCU firmware** → This allows to update Klipper firmware of motherboard when **Katapult** bootloader is installed
	- **4) Update MMB Cubic MCU firmware** → This allows to update Klipper firmware of BigTreeTech MMB Cubic
	- **5) Update Debian packages** → This allows to update installed packages from Debian repository


	### Extras Menu

	<img width="900" src="../assets/images/installer-05.png">


	- **1) Backup Klipper configuration files** →This allows to backup Klipper configuration files to a `backup_klipper.zip` compressed file
	- **2) Restore Klipper configuration files** → This allows to restore Klipper configuration files from a `backup_klipper.zip` compressed file
	- **3) Backup Moonraker database** → This allows to backup Moonraker database to a `backup_moonraker.zip` compressed file
	- **4) Restore Moonraker database** → This allows to restore Moonraker database from a `backup_moonraker.zip` compressed file
	- **5) Restore Web-UI default settings** → This allows to restore the pre-configured settings of Mainsail and Fluidd Web interfaces
	- **6) Delete cache and logs files** → This allows to delete temporary files and log files
	- **7) Extend storage partition** → This allows to extend storage partition to take advantage of the full storage (microSD card or eMMC)

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
