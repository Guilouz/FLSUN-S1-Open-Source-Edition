# FLSUN S1 Open Source Edition
Closed Beta Test

<img width="950" src="https://github.com/user-attachments/assets/62cdfaf2-b0c6-4033-b0c9-dfcff567bf11">

<br /><br />

This Open Source version uses the microSD port of the motherboard to boot on a new OS. Which means that the original OS is not modified. It’s a kind of dual boot, a simple removal of the microSD card allows to boot on the original OS.

This new OS is based on Debian 12 Bookworm and is ready to use.

**What's included:**

  -	Moonraker (latest build without modification)<br />
  -	Klipper (latest build with modifications for S1 support<b>*</b>)<br />
  -	KlipperScreen (latest build with modifications for S1 support)<br />
  -	Mainsail (latest build without modification)<br />
  -	Moonraker Timelapse<br />
  -	MJPG-Streamer<br />
  -	Preconfigured Web interfaces<br />
  -	Improved configuration files with interactive macros<br />
  -	Hostname based on MAC address<br />
  -	Automatic resizing of available space on microSD card<br />

_<b>*</b> All AI features have been removed as they do not work as expected. Only Power Loss Recovery, FLSUN Input Shaper and XY Dimension Calibration features have been kept._

<br />

### TABLE OF CONTENTS:

-	[PREREQUISITES](#prerequisites)
- [MICROSD PREPARATION](#microsd-preparation)
-	[PRINTER PREPARATION](#printer-preparation)
-	[FIRST BOOT](#first-boot)
-	[SSH CONNECTION](#ssh-connection)
-	[WEB INTERFACES](#web-interfaces)
- [CREDITS](#credits)

<br />

## PREREQUISITES

-	MicroSD card with a minimum size of 16GB
-	Raspberry Pi Imager: [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
-	FLSUN OS image: [FLSUN-OS-S1-1.0.img.gz](https://tinyurl.com/y8kctzh5)

<br />

## MICROSD PREPARATION

- Insert the microSD card into your computer.

-	Start **Raspberry Pi Imager**.

-	Click on `CHOOSE OS` button:

    <img width="600" src="https://github.com/user-attachments/assets/8ddad7c1-3669-4961-be57-f44ce926668d">


-	Click on `Use Custom` button and select FLSUN OS image file (with the extension **.gz**):

    <img width="600" src="https://github.com/user-attachments/assets/7761c54f-235f-486e-87f0-4ad6bc6b8ac2">


-	Click on `CHOOSE STORAGE` button and select your microSD card storage:

    <img width="600" src="https://github.com/user-attachments/assets/8c5b41aa-d481-48a8-8d2e-a5a215ca5f90">


-	Click on `NEXT` and select your microSD card storage:

    <img width="600" src="https://github.com/user-attachments/assets/a0acab03-7da4-4224-8196-001f607189ac">


-	When asked if you would like to apply OS customisation settings, click on `NO` button:

    <img width="600" src="https://github.com/user-attachments/assets/b7cb0011-a1b6-4201-8fa7-e92bea6f9933">


-	Then confirm by clicking on `YES` button:

    <img width="600" src="https://github.com/user-attachments/assets/86ca4c99-42f4-4dfc-86ba-662b2cb383fb">


-	Wait until completion and your microSD card is ready.

<br />

## PRINTER PREPARATION

-	Use the H2.0 hex wrench in the accessory box to remove the screws above the screen:

    <img width="900" src="https://github.com/user-attachments/assets/3962a657-3bd1-4f66-a86d-dbbcefd1f536">


-	Use the H3.0 hex wrench in the accessory box to remove the screws under the screen:

    <img width="900" src="https://github.com/user-attachments/assets/f1e1d1eb-3c70-4bc4-87b6-a375eaab8f7e">

 
-	Unplug the display power cord and three data cables:

    <img width="900" src="https://github.com/user-attachments/assets/61092742-02a9-4996-ad55-050bb02245d0">

 
-	Use the H2.0 hex wrench in the accessory box to remove the eight screws on the back cover of the screen, and disassemble the back cover of the screen:

    <img width="900" src="https://github.com/user-attachments/assets/0eb5e970-6a0a-47d3-8315-4c6cacedf86a">


-	Insert your microSD card into the port here:

    <img width="900" src="https://github.com/user-attachments/assets/60f267cd-c9cc-45d9-891d-1de18788b95e">

    <img width="900" src="https://github.com/user-attachments/assets/b108c316-95ed-4437-ad1b-6d2089ad5355">
 
-	You can now screw the screen box back on, reconnect the cables and reattach it to the printer.

<br />

## FIRST BOOT

-	Turn on the printer. You should see the "**Open Source Edition**" boot logo. If not, your image was not correctly written to your microSD card.

-	Once you are on the **KlipperScreen** interface, wait for **Moonraker** and **Klipper** to connect (if not click `Retry` button).

-	Once connected, click on `Configurations` → `Networks` and connect to your WiFi network. Your IP address should be displayed in the top right corner.

-	**WARNING:** Don't forget to calibrate your printer before starting a print. 

 	To do this, go to the `Configurations` → `Calibrations` menu.

    -	**Motors Calibration** → To calibrate the closed loop of the motors
    -	**Z Offset Calibration** → To adjust Z Offset if needed
    -	**Bed Mesh** → To perform Delta calibration and a bed leveling
    -	**Input Shaper** → To measure resonances

-	SSH Access:

    -	root → flsun
    -	pi → flsun

-	Enjoy 😃

<br />

## SSH CONNECTION

-	Download and install the MobaXterm software: [https://mobaxterm.mobatek.net/download-home-edition.html](https://mobaxterm.mobatek.net/download-home-edition.html)

-	Launch it then click on the `Session` icon:

    <img width="900" src="https://github.com/user-attachments/assets/e8a055af-14de-4018-927d-153fb9051f36">

-	Then on then `SSH` icon:

    <img width="900" src="https://github.com/user-attachments/assets/25c3f848-826f-4394-b0c5-ab8a68de95ad">
 
-	Enter the IP address of your printer in the `Remote Host` field, check the `Specify username` box and enter the username **pi** in the field then click on `OK`:

    <img width="900" src="https://github.com/user-attachments/assets/2f0eaaf8-4084-43be-840c-4ee6cb9ced63">

-	On the new displayed window, enter the password **flsun** (it's not displayed when typing, this is normal).

-	An authorization window will appear, authorize it. It's also possible that another window asking you to change the password will appear, ignore it.

-	Once connected, on the left part of the window you have access to the folders and files of your printer and on the right part to the SSH command prompt window:

    <img width="900" src="https://github.com/user-attachments/assets/8864f881-d30a-4165-b6e1-8bfa0b56cb54">

<br />
 
## WEB INTERFACES

By default, Mainsail is installed on port 80. You can also install Fluidd.

- **You have two possibilities:**

  -	Keep Mainsail and install Fluidd on port 81
  -	Remove Mainsail and install Fluidd on port 80

-	Connect to printer over SSH.

-	Start **Kiauh** by entering this command: 

    ```
    ./kiauh/kiauh.sh
    ```

    <img width="450" src="https://github.com/user-attachments/assets/8460ccae-e19a-4fcd-b124-b59d2791988c">

 
-	**To keep Mainsail and install Fluidd on port 81:**

    -	Enter **1** for Install menu → **4** for Fluidd → Enter **81** for port number → Enter **N** to not install the recommended macros

    You can access to **Mainsail** with `http://xxx.xxx.xx.xxx/` (replacing **xxx.xxx.xxx.xxx** by your local IP address).<br>
    You can access to **Fluidd** with `http://xxx.xxx.xx.xxx:81/` (replacing **xxx.xxx.xxx.xxx** by your local IP address).

-	**To remove Mainsail and install Fluidd on port 80:**

    -	Enter **3** for Remove menu → **3** for Mainsail → **B** to go back → **1** for Install menu → **4** for Fluidd → Enter **N** to not install the recommended macros

    You can access to **Fluidd** with `http://xxx.xxx.xx.xxx/` (replacing xxx.xxx.xxx.xxx by your local IP address).

<br />

## CREDITS

- [Guilouz](https://github.com/Guilouz)

- [Taiwan22](https://github.com/Taiwan22)
