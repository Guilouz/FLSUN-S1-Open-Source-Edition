---
icon: material/printer-3d
---

## Settings for Bed Mesh Selection
<hr>

In order for the Bed Mesh Selection to work it's necessary to modify the Start Gcode.

### OrcaSlicer
<hr>

- Go to **Printer Settings** → **Machine G-code** → **Start G-code**

- And replace existing Gcode by this one:

    ```
    SET_PRINT_STATS_INFO TOTAL_LAYER=[total_layer_count]
	_START_GCODE X_MIN={first_layer_print_min[0]} X_MAX={first_layer_print_max[0]} Y_MIN={first_layer_print_min[1]} Y_MAX={first_layer_print_max[1]} BED_TEMP=[first_layer_bed_temperature] HOTEND_TEMP=[first_layer_temperature]
    ```
 
 - Go to **Printer Settings** → **Machine G-code** → **End G-code**

- And replace existing Gcode by this one:

    ```
    _END_GCODE
    ```

 - Go to **Printer Settings** → **Machine G-code** → **Layer change G-code**
 
 - And add this Gcode:
 
    ```
    SET_PRINT_STATS_INFO CURRENT_LAYER={layer_num + 1}
    ```


### FlsunSlicer
<hr>

- Go to **Printer Settings** → **Machine G-code** → **Start G-code**

- And replace existing Gcode by this one:

    ```
    SET_PRINT_STATS_INFO TOTAL_LAYER=[total_layer_count]
	_START_GCODE X_MIN={first_layer_print_min[0]} X_MAX={first_layer_print_max[0]} Y_MIN={first_layer_print_min[1]} Y_MAX={first_layer_print_max[1]} BED_TEMP=[first_layer_bed_temperature] HOTEND_TEMP=[first_layer_temperature]
	;is_AB
    ;is_AB
    ```
 
 - Go to **Printer Settings** → **Machine G-code** → **End G-code**

- And replace existing Gcode by this one:

    ```
    _END_GCODE
    ```

 - Go to **Printer Settings** → **Machine G-code** → **Layer change G-code**
 
 - And add this Gcode:
 
    ```
    SET_PRINT_STATS_INFO CURRENT_LAYER={layer_num + 1}
    ```


###  PrusaSlicer / SuperSlicer
<hr>

- Go to **Printer Settings** → **Custom G-code** → **Start Gcode**

- And replace existing Gcode by this one:

    ```
    SET_PRINT_STATS_INFO TOTAL_LAYER=[total_layer_count]
    _START_GCODE X_MIN={first_layer_print_min[0]} X_MAX={first_layer_print_max[0]} Y_MIN={first_layer_print_min[1]} Y_MAX={first_layer_print_max[1]} BED_TEMP=[first_layer_bed_temperature] HOTEND_TEMP=[first_layer_temperature]
    ```

- Go to **Printer Settings** → **Custom G-code** → **End Gcode**

- And replace existing Gcode by this one:

    ```
    _END_GCODE
    ```

 - Go to **Printer Settings** → **Custom G-code** → **After layer change Gcode**
 
 - And add this Gcode:
 
    ```
    SET_PRINT_STATS_INFO CURRENT_LAYER={layer_num + 1}
    ```


## Settings for Timelapse
<hr>

Timelapse feature is enabled by default but to use the **layermacro** mode which grabs a frame every layer change you need to add the **`TIMELAPSE_TAKE_FRAME`** macro to your slicer so that it is added to the Gcode before a layer change.

### OrcaSlicer / FlsunSlicer
<hr>

- Go to **Printer Settings** → **Machine G-code** → **Before layer change G-code**

    ```
	;BEFORE_LAYER_CHANGE
	;[layer_z]
	G92 E0
	TIMELAPSE_TAKE_FRAME
    ```

###  PrusaSlicer / SuperSlicer
<hr>

- Go to **Printer Settings** → **Custom G-code** → **Before layer change Gcode**

- And replace existing Gcode by this one:

    ```
	;BEFORE_LAYER_CHANGE
	;[layer_z]
	G92 E0
	TIMELAPSE_TAKE_FRAME
    ```

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
