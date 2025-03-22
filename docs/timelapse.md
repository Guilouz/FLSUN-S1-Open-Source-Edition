---
icon: material/video
hide:
  - toc
---
Timelapse is a 3rd party Moonraker component to create timelapse of 3D prints.<br />
It can be enabled with **Easy Installer**. See <a href="../klipper-configurations-files">:material-file-restore: Klipper Configurations Files</a> section but if you need to configure it manually follow these steps.

- Connect to printer over SSH (see <a href="../ssh-connection">:material-console: SSH Connection</a> section).

- In the SSH command prompt window, enter the following command:

	``` title="SSH Command Prompt"
	ln -srfn "/home/pi/moonraker-timelapse/klipper_macro/timelapse.cfg" "/home/pi/printer_data/config/timelapse.cfg"
	```

- Open **`config.cfg`** file:

    - On **Mainsail** Web Interface go to **`MACHINE`** tab on the left side.
    - On **Fluidd** Web Interface go to **`Configuration`** icon on the left side.

- Remove the first **`#`** symbol at the following line:

    ``` title="config.cfg" hl_lines="8"
    #######################################################
    # Timelapse Configuration
    #######################################################
    
    # If you want to enable Timelapse -> Enable 'timelapse.cfg'
    # ---------------------------------------------------------
    
    #[include timelapse.cfg]
    ```

- Click on **`SAVE & RESTART`** at the top right to save the file.

- Open **`moonraker.conf`** file:

    - On **Mainsail** Web Interface go to **`MACHINE`** tab on the left side.
    - On **Fluidd** Web Interface go to **`Configuration`** icon on the left side.

- Remove the first **`#`** symbol at the following lines:

    ``` title="moonraker.conf"
    #[timelapse]
    #output_path: ~/printer_data/timelapse
    #frame_path: /tmp/timelapse

    #[update_manager timelapse]
    #type: git_repo
    #primary_branch: main
    #path: ~/moonraker-timelapse
    #origin: https://github.com/mainsail-crew/moonraker-timelapse.git
    #managed_services: klipper moonraker
    ```

- Click on **`SAVE & RESTART`** at the top right to save the file.

- Make sure you have configured you slicer for Timelapse, see <a href="../slicers-settings/#settings-for-timelapse">:material-printer-3d: Slicers Settings</a>section.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
