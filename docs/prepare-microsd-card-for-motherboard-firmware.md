---
icon: material/micro-sd
---

Motherboard firmware needs to be updated to support the latest version of Klipper.

!!! Warning
    If you have flashed the motherboard with the firmware provided by FLSUN (in the Silent Kit guide) which overrides the bootloader and prevents the use of the microSD port, go directly to <a href="../flash-motherboard-firmware/#flash-with-st-link-v2-alternative">:octicons-cpu-16: Flash Motherboard Firmware</a> section.

## Prerequisites
<hr>

- microSD card with small capacity (e.g. 128MB or 256MB, larger capacity may not work)
- Motherboard firmware for Open Source Edition: <a href="../assets/downloads/firmwares/open-source-edition/Robin_nano35.bin" >:material-download: Robin_nano35.bin</a>

## Prepare microSD
<hr>

- Insert the microSD card with small capacity into your computer.

- Format it in FAT32 and an allocation size of 4096 (if available).

- Copy **`Robin_nano35.bin`** file to the root of the microSD card, then you can remove it from your computer.

- Next, follow <a href="../flash-motherboard-firmware">:octicons-cpu-16: Flash Motherboard Firmware</a> section.

<br /> 

**You can also compile your own firmware:**

!!! IMPORTANT
    MCUs have limited write cycles (>about 10K cycles for a STM32 chip). Updating the firmware with each Klipper release could shorten the life of your MCU!<br /><br />
    <i>**When is it necessary to update Klipper firmware?**</i>
    Every time Klipper mentions to update the MCU at startup, no more.


- Connect to printer over SSH (see <a href="../ssh-connection">:material-console: SSH Connection</a> section).

- In the SSH command prompt window, enter the following commands (one at a time):

    ``` title="SSH Command Prompt"
    cd ~/klipper/
    ```
    ``` title="SSH Command Prompt"
    make menuconfig
    ```

- Move on the menu with the ++"↑"++ and ++"↓"++ keys of your keyboard and validate the selected item with the ++"Enter"++ key and select these settings:

    <img width="800" src="../assets/images/klipper-fw-config.png">


- Then on your keyboard press the ++"Q"++ key then ++"Y"++ to save configuration.

- Enter the following commands to compile firmware (one at a time):

    ``` title="SSH Command Prompt"
    make clean
    ```
    ``` title="SSH Command Prompt"
    make
    ```

- Then this one to convert firmware:

    ``` title="SSH Command Prompt"
    ./scripts/update_mks_robin.py out/klipper.bin out/Robin_nano35.bin
    ```

- Get the firmware named **`Robin_nano35.bin`** in **`/home/pi/klipper/out/`** directory (on the left panel of **MobaXterm**, right click on the file and select `Download`).

- Copy **`Robin_nano35.bin`** file to the root of the microSD card.

- Next, follow <a href="../flash-motherboard-firmware">:octicons-cpu-16: Flash Motherboard Firmware</a> section.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
