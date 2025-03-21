---
icon: material/lightbulb-on
---

### Lock Screen
<hr>

You can lock the screen with password. Note this is not a secure system, it's saved as plain text in **KlipperScreen** configuration file, but it's intended to deter children or people present when printing.

- Open **`KlipperScreen.conf`** file:

	- On **Mainsail** Web Interface go to **`MACHINE`** tab on the left side.
	- On **Fluidd** Web Interface go to **`Configuration`** icon on the left side.

- Remove the **`#`** symbol before **`lock_password `** setting and define pasword you want (by default: **flsun**):

	``` title="KlipperScreen.conf" hl_lines="4"
	[main]
	# Set the password to use when locking the screen, this is not a secure system, it's saved as plain text,
	# but it's intended to deter children or people present when printing.
	#lock_password: flsun
	```

- Once done, click on **`SAVE & RESTART`** button at the top right to save the file.

- You can now lock the screen on **Shutdown Panel** when is needed:

	<img width="600" src="../assets/images/screenshot_20.png">


### Power Button
<hr>

You can control the short press of the power button (right of the screen).

- Open **`macros.cfg`** file in **`Configurations`** folder:

	- On **Mainsail** Web Interface go to **`MACHINE`** tab on the left side.
	- On **Fluidd** Web Interface go to **`Configuration`** icon on the left side.

- And edit this macro by replacing the Gcode command with whatever you want to run when you short press the power button:

	``` title="macros.cfg" hl_lines="4"
	[gcode_macro _PWR_KEY]
	description: Short press for power button
	gcode:
	  M117 Short Press done!
	```

- Once done, click on **`SAVE & RESTART`** button at the top right to save the file.

!!! Note
    By default, a long press on the power button power off the system.


### Take a Screenshot
<hr>

You can take a screenshot of KlipperScreen.

- Open your Web interface and:

    - On **Mainsail** Web Interface go to **`CONSOLE`** tab on the left side.
    - On **Fluidd** Web Interface go to **`Console`** icon on the left side.

- Enter this command:

    ``` title="Console"
    _SCREENSHOT
    ```

- A screenshot will be saved every time the command is executed in the folder:

	**/home/pi/printer_data/config/screenshots**
	
	!!! Note
	    You can take many screenshots, they will be saved as <i>screenshot_001.png</i>, <i>screenshot_002.png</i>, etc...

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
