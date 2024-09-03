# FLSUN S1 Open Source Edition
Closed Beta Test

<img width="950" src="https://github.com/user-attachments/assets/62cdfaf2-b0c6-4033-b0c9-dfcff567bf11">

<br /><br />

This **FLSUN-OS** is an Open Source version uses the microSD port of the core board to boot on a new OS. Which means that the original OS is not modified. It’s a kind of dual boot, a simple removal of the microSD card allows to boot on the original OS.

This new OS is based on Debian 12 Bookworm and is ready to use.

Benchmark comparison between **STOCK OS** (Board flsun) and our **FLSUN-OS**: [Geekbench.com](https://browser.geekbench.com/v5/cpu/compare/22823940?baseline=22823878)

**What's included:**

  -	Moonraker (latest build without modification)<br />
  -	Klipper (latest build with modifications for S1 support<b>*</b>)<br />
  -	KlipperScreen (latest build with modifications for S1 support)<br />
  -	Mainsail (latest build without modification)<br />
  -	Moonraker Timelapse<br />
  -	MJPG-Streamer (latest build)<br />
  -	Preconfigured Web interfaces<br />
  -	Improved configuration files with interactive macros<br />
  -	Hostname based on MAC address<br />
  -	Automatic resizing of available space on microSD card<br />

_<b>*</b> All AI features have been removed as they do not work as expected. Only Power Loss Recovery, FLSUN Input Shaper and XY Dimension Calibration features have been kept._

<img width="700" src="https://github.com/user-attachments/assets/fc4dd3cd-576a-4edf-9dd9-cc90293d9f3b">

<br />

### TABLE OF CONTENTS:

-	:clipboard: [CHANGELOGS](#clipboard-changelogs)
-	:stars: [SCREENSHOTS](#stars-screenshots)
-	:memo: [PREREQUISITES](#memo-prerequisites)
- :floppy_disk: [MICROSD PREPARATION FOR FLSUN OS](#floppy_disk-microsd-preparation-for-flsun-os)
- :floppy_disk: [MICROSD PREPARATION TO FLASH MOTHERBOARD FIRMWARE](#floppy_disk-microsd-preparation-to-flash-motherboard-firmware)
- :zap: [FLASH MOTHERBOARD FIRMWARE](#zap-flash-motherboard-firmware)
-	:wrench: [INSERTING MICROSD CARD FOR FLSUN OS](#wrench-inserting-microsd-card-for-flsun-os)
-	:electric_plug: [FIRST BOOT](#electric_plug-first-boot)
-	:link: [SSH CONNECTION](#link-ssh-connection)
-	:globe_with_meridians: [WEB INTERFACES](#globe_with_meridians-web-interfaces)
-	:camera: [ENABLE CAMERA SETTINGS MACROS](#camera-enable-camera-settings-macros)
-	:triangular_ruler: [XY DIMENSION CALIBRATION](#triangular_ruler-xy-dimension-calibration)
-	:movie_camera: [USE TIMELAPSE](#movie_camera-use-timelapse)
-	:clock130: [UPDATE TIME ZONE](#clock130-update-time-zone)
-	:earth_americas: [REMOTE ACCESS](#earth_americas-remote-access)
- :star: [CREDITS](#star-credits)

<br />

**Discussions about this project: [Here](https://github.com/Guilouz/FLSUN-Open-Source-Edition/discussions)**

<br />

## :clipboard: CHANGELOGS

**03/09/2024:**

- **KlipperScreen:**
	- Improved `Unload` panel:
   
	  <img width="700" src="https://github.com/user-attachments/assets/04664eee-fa77-47d2-a6d3-7095ba8bb5fa">


**01/09/2024:**

- **New FLSUN OS image version 1.1:**
	- Updated kernel to restore CPU frequency to 1.5GHz instead of 1GHz (50% increase in performance).
	- Disabled Wi-Fi Power Management, this frees up bandwidth, and increases camera fps.
	- Integration of GuppyFLO, a lightweight self-hosted service that allows remote management via TCP Proxy using Moonraker and Tailscale. See [REMOTE ACCESS](#earth_americas-remote-access) section.
	- Replaced hostname FLSUN-OS-XXXX with FLSUN-S1-XXXX (still based on MAC address).
	- Improved SSH header.
	- Updated Klipper configuration files.
	- Updated Web interface configuration files.
	- Integration of FLSUN Gcodes files (Slicer displayed is OrcaSlicer just to have support for info and thumbnails but these are the original Gcodes).
   	- Fixed screen brightness.

- **KlipperScreen:**
	- Fixed screen brightness after reboot.
	- Improved UI.

**30/08/2024:**

<details>
<summary>Show / Hide</summary>

- **Klipper configurations files:**

  - Fixed macros for `M600`.
  - Minor fixes.

  **Note: Make sure you use latest Klipper configuration files.**

</details>

**29/08/2024:**

<details>
<summary>Show / Hide</summary>

- **KlipperScreen**:

  - Improved retrieval of drying box information (improves fluidity). 
  - Added prompt for filament unloading process.
  - Now possible to load or unload filament at the desired temperature.
  - Improved UI.

- **Klipper configurations files:**

  - Improved `UNLOAD_FILAMENT` & `UNLOAD_FILAMENT` macros.
  - Increased motion sensor detection length.
  - Disabled extruder motor when calibrating resonances.
  - Added settings for sensors in KlipperScreen.conf.
  - Minor fixes.

  **Note: Make sure you use latest Klipper configuration files.**

</details>

**24/08/2024:**

<details>
<summary>Show / Hide</summary>

- **Klipper**:

  - Added support for XY Dimension Calibration with `M101` command:
    - **M101 S0** → Reset XY Offsets
    - **M101 X**zz **T**zz → Define X Offset (X → Measured Size - T → Target Size)
    - **M101 Y**zz **T**zz → Define Y Offset (Y → Measured Size - T → Target Size)

- **Klipper configurations files:**
  
  - Updated to include `CALIBRATION_X_OFFSET`, `CALIBRATION_Y_OFFSET` and `CALIBRATION_RESET_XY_OFFSETS` macros

- **KlipperScreen**:

  - UI now show Spool Weight in grams (setting added to display it in percentage).

</details>

<br />

## :stars: SCREENSHOTS

<details>
<summary>Show / Hide</summary>
<br />

- **Main Menu**

    <img width="600" src="https://github.com/user-attachments/assets/fc4dd3cd-576a-4edf-9dd9-cc90293d9f3b">

- **Move Menu**

    <img width="600" src="https://github.com/user-attachments/assets/7789ff3f-60a4-46b2-8d6c-28f9bfd973af">

- **Temperature Menu**

    <img width="600" src="https://github.com/user-attachments/assets/f10a6ff9-45a0-4dd5-8b8f-db815cfd05f7">

- **Extrude Menu**

    <img width="600" src="https://github.com/user-attachments/assets/b2d77b6d-a8fe-4b71-b2ab-041550fd22ca">

- **Print Menu**

    <img width="600" src="https://github.com/user-attachments/assets/eed3b0e3-35bc-4bb7-84ec-f649f0b6abfa">

- **Configurations Menu**

    <img width="600" src="https://github.com/user-attachments/assets/dc42b935-d5f9-4a88-bdcf-13377611a229">

- **Calibrations Menu**

    <img width="600" src="https://github.com/user-attachments/assets/76d99fbf-bd1e-4cdd-b7a4-3804ff796a4c">

- **Drying Box Menu**

    <img width="600" src="https://github.com/user-attachments/assets/788bf911-a24d-4f69-8941-791075ca3946">


</details>

<br />

## :memo: PREREQUISITES

-	microSD card with small capacity (e.g. 128MB or 256MB) to flash motherboard firmware
-	microSD card with a minimum size of 16GB for FLSUN OS (I recommend SanDisk Extreme PRO)

<br />

## :floppy_disk: MICROSD PREPARATION FOR FLSUN OS

-	Download and install **Raspberry Pi Imager**: [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
  
-	Download **FLSUN OS** image: [Releases](https://github.com/Guilouz/FLSUN-Open-Source-Edition/releases)

- Insert the microSD card into your computer.

-	Start **Raspberry Pi Imager**.

-	Click on `CHOOSE OS` button:

    <img width="600" src="https://github.com/user-attachments/assets/8ddad7c1-3669-4961-be57-f44ce926668d">


-	Click on `Use Custom` button and select **FLSUN OS** image file (with the extension **.gz**):

    <img width="600" src="https://github.com/user-attachments/assets/7761c54f-235f-486e-87f0-4ad6bc6b8ac2">


-	Click on `CHOOSE STORAGE` button and select your microSD card storage:

    <img width="600" src="https://github.com/user-attachments/assets/8c5b41aa-d481-48a8-8d2e-a5a215ca5f90">


-	Click on `NEXT` and select your microSD card storage:

    <img width="600" src="https://github.com/user-attachments/assets/a0acab03-7da4-4224-8196-001f607189ac">


-	When asked if you would like to apply OS customisation settings, click on `NO` button:

    <img width="600" src="https://github.com/user-attachments/assets/b7cb0011-a1b6-4201-8fa7-e92bea6f9933">


-	Then confirm by clicking on `YES` button:

    <img width="600" src="https://github.com/user-attachments/assets/86ca4c99-42f4-4dfc-86ba-662b2cb383fb">


- Wait until the operation is completed and your microSD card is ready, then you can remove it from your computer.

<br />

## :floppy_disk: MICROSD PREPARATION TO FLASH MOTHERBOARD FIRMWARE

Motherboard firmware need to be updated to support latest Klipper version.

- Insert the microSD card with small capacity into your computer.

- Format it in FAT32 and an allocation size of 4096.

- Download the motherboad firmware: [Robin_nano35.bin for Open Source Edition](https://github.com/Guilouz/FLSUN-Open-Source-Edition/raw/main/Motherboard%20Firmwares/Open%20Source%20Edition/Robin_nano35.bin)

- Copy `Robin_nano35.bin` file to the root of the microSD card, then you can remove it from your computer.

<br />

## :zap: FLASH MOTHERBOARD FIRMWARE

- Make sure the printer is turned off.

-	Use the H2.0 hex wrench in the accessory box to remove the screws from the top cover of the printer.

- Insert microSD card into the microSD port on the motherboard:

    <img width="900" src="https://github.com/user-attachments/assets/9b02b7a9-1088-4c56-a962-48b4a3e488a9">

- Turn on the printer and wait a few seconds, the flash will be done automatically.

- Installation only takes a few seconds, to verify that the firmware has been successfully installed, the file on the microSD card must have been renamed to `ROBIN_NANO35.BIN.CUR`.

- Turn off the printer, you can remove the microSD card and screw the printer top cover back on.

**Note:** If you want to go back to stock OS you need to reflash motherboad with this firmware: [Robin_nano35.bin for Stock OS](https://github.com/Guilouz/FLSUN-Open-Source-Edition/raw/main/Motherboard%20Firmwares/Stock/Robin_nano35.bin)

<br />

## :wrench: INSERTING MICROSD CARD FOR FLSUN OS

- Make sure the printer is turned off.

-	Use the H2.0 hex wrench in the accessory box to remove the screws from the top cover of the printer.

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

## :electric_plug: FIRST BOOT

-	Turn on the printer. You should see the "**Open Source Edition**" boot logo. If not, your image was not correctly written to your microSD card.

-	Once you are on the **KlipperScreen** interface, wait for **Moonraker** and **Klipper** to connect (if not click `Retry` button). The LEDs on the left side of the screen should light up white as soon as the connection is established.

-	Once connected, click on `Configurations` → `Network` and connect to your WiFi network. Your IP address should be displayed in the top right corner.

- Then, restart the printer.

-	**:bangbang: WARNING:** Don't forget to calibrate your printer before starting a print. 

 	To do this, go to the `Configurations` → `Calibrations` menu.

    -	**Motors Calibration** → To calibrate the closed loop of the motors
    -	**Z Offset Calibration** → To adjust Z Offset if needed
    -	**Bed Mesh** → To perform Delta calibration and a bed leveling
    -	**Input Shaper** → To measure resonances

-	SSH Access:

    -	root → flsun
    -	pi → flsun

-	Enjoy :smiley:

<br />

## :link: SSH CONNECTION

-	Download and install the **MobaXterm** software: [https://mobaxterm.mobatek.net/download-home-edition.html](https://mobaxterm.mobatek.net/download-home-edition.html)

-	Launch it then click on the `Session` icon:

    <img width="900" src="https://github.com/user-attachments/assets/e8a055af-14de-4018-927d-153fb9051f36">

-	Then on then `SSH` icon:

    <img width="900" src="https://github.com/user-attachments/assets/25c3f848-826f-4394-b0c5-ab8a68de95ad">
 
-	Enter the IP address of your printer in the `Remote Host` field, check the `Specify username` box and enter the username **pi** in the field then click on `OK`:

    <img width="900" src="https://github.com/user-attachments/assets/2f0eaaf8-4084-43be-840c-4ee6cb9ced63">

-	On the new displayed window, enter the password **flsun** (it's not displayed when typing, this is normal).

-	An authorization window will appear, authorize it. It's also possible that another window asking you to change the password will appear, ignore it.

-	Once connected, on the left part of the window you have access to the folders and files of your printer and on the right part to the SSH command prompt window:

    <img width="900" src="https://github.com/user-attachments/assets/6e32678c-c170-418e-91e4-621126322885"><


<br />
 
## :globe_with_meridians: WEB INTERFACES

By default, **Mainsail** is installed on port 80. You can also install **Fluidd**.

| Mainsail |
| :---------: |
| <img width="1000" src="https://github.com/user-attachments/assets/22d7a89a-0565-42ea-94a0-5ed454a39f4d"> |

| Fluidd |
| :---------: |
| <img width="1000" src="https://github.com/user-attachments/assets/5ffd08bd-aeb9-4ebf-8cd2-9f6661886de2"> |

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

    You can access to **Fluidd** with `http://xxx.xxx.xx.xxx/` (replacing **xxx.xxx.xxx.xxx** by your local IP address).

<br />

## :camera: ENABLE CAMERA SETTINGS MACROS

Camera Settings macros are not enabled by default. To enable them:

- Go to your **Mainsail** Web interface then click on `MACHINE` tab.

- Then, open the `printer.cfg` file and remove the first **#** symbol at the following line:

    ```
    #[include camera_settings.cfg] # Remove comment to use macros to control camera settings
    ```

- Click on `SAVE & RESTART` at the top right to save the file.

<br />

## :triangular_ruler: XY DIMENSION CALIBRATION

This can be useful if the accuracy of your dimensions is not acceptable.

- Make sure you have latest **Klipper** version in `Update Manager`.

- Download this calibration cube: <a href="https://www.printables.com/model/118657-calibration-cube">Printables</a>

- Slice it and print it.

- Once printed, measure the X and Y dimensions. The ideal values ​​of this model are: X=20mm / Y=20mm.

- If you notice a significant deviation in the measured dimensions, it will therefore be necessary to apply a correction.

- Go to your **Mainsail** Web interface then select the `CONSOLE` tab on the left side.

- Enter this command to reset X/Y Offsets if one of them is already applied:

  ```
  M101 S0
  ```

- Wait for **Klipper** to restart.

- If you notice a deviation in X, enter this command by replacing `zz`  by your measured value in millimeters in X (Note: T is the expected value, here 20mm):

  ```
  M101 Xzz T20
  ```

- Wait for **Klipper** to restart.

- If you notice a deviation in Y, enter this command by replacing `zz`  by your measured value in millimeters in Y (Note: T is the expected value, here 20mm):
 
  ```
  M101 Yzz T20
  ```

- Wait for **Klipper** to restart.

- Correction is now applied in your `printer.cfg` file. You can reprint your model to see if the accuracy of your dimensions is now acceptable.

<br />

## :movie_camera: USE TIMELAPSE

Timelapse feature is enabled by default but to use the **layermacro** mode which grabs a frame every layer change you need to add the `TIMELAPSE_TAKE_FRAME` macro to your slicer so that it is added to the Gcode before or after a layer change.

- **OrcaSlicer:**

    Go to Printer Settings → Machine G-code → Before layer change G-code → Add **TIMELAPSE_TAKE_FRAME**

- **FlsunSlicer / PrusaSlicer / SuperSlicer:**

    Go to Printer Settings → Custom G-code → Before layer change Gcode → Add **TIMELAPSE_TAKE_FRAME**

<br />

## :clock130: UPDATE TIME ZONE

To change time zone, follow these instructions:

- In the SSH command prompt window, enter the following command to check the current time zone:

  ```
  timedatectl
  ```

- You can change your time zone by entering this command:
  
  ```
  sudo dpkg-reconfigure tzdata
  ```

- On the page that appears, select your geographic area from the list and press `Enter`.

- Then select your time zone in the new list and press `Enter`.

- You can then verify that the change has been taken into account by retyping this command:
  
  ```
  timedatectl
  ```

<br />

## :earth_americas: REMOTE ACCESS

**GuppyFLO** is a lightweight self-hosted service that allows remote management via TCP Proxy using Moonraker and Tailscale.

To remotely access your machine, follow these steps:

- In the SSH command prompt window, enter the following command to start installation of **GuppyFLO**:

  ```
  sudo ./guppyflo/guppyflo.sh
  ```

- Type `1` then `Enter`:

  <img width="720" src="https://github.com/user-attachments/assets/0527c5fe-2398-402f-8eb1-a55a39329370">

- After installation you get this:

  <img width="720" src="https://github.com/user-attachments/assets/6a6168f8-0f68-40af-84ec-c87addb51a19">

- Then go to this address to connect to your **Tailscale** account or create one: [https://login.tailscale.com/start](https://login.tailscale.com/start)

- Once logged in, go to this address and enable the `MagicDNS` feature: [https://login.tailscale.com/admin/dns](https://login.tailscale.com/admin/dns)

  <img width="720" src="https://github.com/user-attachments/assets/44ed45fb-f292-4274-acad-5cdafe384232">

- You can now connect your printer to your Tailscale account by going to the address given in **step 3** and clicking the `Connect` button:

  <img width="552" alt="04" src="https://github.com/user-attachments/assets/6c7045c6-cf8f-441c-81f6-22c6ff6cb054">

- On your **Tailscale** dashboard you can now see your connected printer:

  <img width="1000" src="https://github.com/user-attachments/assets/126dd8dc-c708-4e12-8423-981509ed5068">

- You can change the name of the printer (the name corresponds to the url you will access to connect remotely):

  <img width="1000" src="https://github.com/user-attachments/assets/356e5ada-ede1-4d34-9afb-ae59161e1cc3">

- Disable `Auto-generate from OS hostname`, enter the desired name and click on `Update name` button:

  <img width="502" src="https://github.com/user-attachments/assets/5e739b8e-7d61-4831-b4b6-4b988b11831b">

- Now install the **Tailscale** client on the device from which you want to access your printer by going to this address: [https://tailscale.com/download](https://tailscale.com/download)

- Sign-in and connect your client to your **Tailscale** account (here I use my mobile):

  <img width="350" src="https://github.com/user-attachments/assets/2f82931a-562c-4f33-bb3f-93749c0aa90a">

- You can now remotely connect to your printer with the following addresses:

    You can access to **Mainsail** with `http://gyppyflo/` (by default) or with your custom hostname, here: `http://flsun-s1/`.<br>
    You can access to **Fluidd** with `http://guppyflo:81/` (by default) or with your custom hostname, here: `http://flsun-s1:81/`.

  <img width="350" src="https://github.com/user-attachments/assets/fd6ae6d7-a659-410c-9af3-146bd4c44894"> <img width="350" src="https://github.com/user-attachments/assets/b50ee302-ee51-43c5-8c13-91ae01e743f4">

- If you want to disable **GuppyFLO**, run the installer again and type `2` then `Enter`.

<br />

## :star: CREDITS

- [Guilouz](https://github.com/Guilouz)

- [Taiwan22](https://github.com/Taiwan22)
