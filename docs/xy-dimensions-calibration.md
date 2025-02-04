---
icon: material/ruler-square-compass
hide:
  - toc
---

This can be useful if the accuracy of your dimensions is not acceptable.

- Download this calibration cube: <a href="../assets/downloads/Calibration_Cube.stl">:material-download: Calibration_Cube.stl</a>

- Slice it and print it.

- Once printed, measure the X and Y dimensions. The ideal values ​​of this model are: X=20mm / Y=20mm.

- If you notice a significant deviation in the measured dimensions, it will therefore be necessary to apply a correction:

	- Open your Web Interface:

    - Run **`CALIBRATION_RESET_XY_OFFSETS`** macro to reset existing values:

		<img width="450" src="../assets/images/xy-dimensions-01.png">

	- Wait for **Klipper** to restart.

	- If you notice a deviation in X,  click on the down arrow at the **`CALIBRATION_X_OFFSET`** macro:

		<img width="450" src="../assets/images/xy-dimensions-02.png">


	- Enter the value you measured in **X** (in millimeters) and click the **`SEND`**  button:

		<img width="250" src="../assets/images/xy-dimensions-03.png">

	- Wait for **Klipper** to restart.
	
	- Correction is now applied for **X** axis in your **`printer.cfg`** file.

	- If you notice a deviation in Y,  click on the down arrow at the **`CALIBRATION_Y_OFFSET`** macro:

		<img width="450" src="../assets/images/xy-dimensions-04.png">


	- Enter the value you measured in **Y** (in millimeters) and click the **`SEND`**  button:

		<img width="250" src="../assets/images/xy-dimensions-05.png">

	- Wait for **Klipper** to restart.
	
	- Correction is now applied for **Y** axis in your **`printer.cfg`** file.

	- You can reprint your model to see if the accuracy of your dimensions is now acceptable.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
