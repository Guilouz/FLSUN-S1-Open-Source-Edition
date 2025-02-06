---
icon: material/printer-3d-nozzle
---

On an extruder, the **rotation_distance** is the amount of distance the filament travels for one full rotation of the stepper motor. The best way to get an accurate value for this setting is to use a "measure and trim" procedure.

### Procedure
<hr>

- Remove PTFE tube from the Extruder for the measure.

- Heat the Hotend to an appropriate temperature and insert filament in it.

- Use a marker to place a mark on the filament 120mm from the inlet of the extruder.

- Then use a digital caliper to measure the actual distance from that mark as accurately as possible.

    Note this value of 120mm as the **`<initial_mark_distance>`**.

- Go to you Web interface:

    - On **Mainsail** Web Interface go to **`CONSOLE`** tab on the left side.
    - On **Fluidd** Web Interface go to **`Console`** icon on the left side.

- Extrude 100mm of filament with the following command sequence:

    ```
    G91
    ```

    ```
    G1 E100 F100
    ```

    Note this value of 100mm as the **`<requested_extrude_distance>`**.

- Wait for extruder to complete the movement (this will take several seconds). It's important to use a slow extrusion speed for this test, as a faster speed can cause high pressure in the extruder which will skew the results. So don't use the EXTRUDE button from Mainsail/Fluidd or from the screen for this test as they extrude at a fast rate.

- Then use a digital caliper to measure the new distance from the inlet of the extruder to the mark on the filament.

    Note this value as **`<measured_distance>`**.

- Then calculate:

    **`<initial_mark_distance>`** :fontawesome-solid-minus: **`<measured_distance>`** :fontawesome-solid-arrow-right-long: **`<extrusion_distance>`**

- Then retrieve the current **rotation_distance** value from the `printer.cfg` file at the `rotation_distance:` line of the `[extruder]` section:

    ``` title="printer.cfg" hl_lines="6"
    [extruder]
	step_pin: PE0
	dir_pin: !PB9
	enable_pin: !PE4
	microsteps: 16
	rotation_distance: 4.5
    ```

    Note this value as `<current_rotation_distance>`.

- Calculate the rotation_distance as follows:

    **`<current_rotation_distance>`** :fontawesome-solid-xmark: **`<extrusion_distance>`** :fontawesome-solid-divide: **`<requested_extrude_distance>`** :fontawesome-solid-arrow-right-long: **`<rotation_distance>`**

- Then replace the new value in the **`printer.cfg`** file by rounding the new **`rotation_distance`** to three decimal places.

- You can now retract filament and replace your PTFE tube in its place, your extruder is calibrated.


### Example
<hr>

- After extruding 100mm, I measure a distance of 18 mm between the inlet of my extruder and the mark on the filament.

- So I have :

    - My **`<initial_mark_distance>`** value of 120mm.
    - My **`<requested_extrude_distance>`** value of 100mm.
    - My **`<measured_distance>`** value of 18mm.

- So I calculate my current **`<extrusion_distance>`** for 100mm requested:

    **`<initial_mark_distance>`** :fontawesome-solid-minus: **`<measured_distance>`** :fontawesome-solid-arrow-right-long: **`<extrusion_distance>`**

    120mm :fontawesome-solid-minus: 18mm :fontawesome-solid-arrow-right-long: **102mm**

- I get the **`<current_rotation_distance>`** value from the **`printer.cfg`** file which is **4.5**.

- So I then calculate my new **`<rotation_distance>`** value:

    **`<current_rotation_distance>`** :fontawesome-solid-xmark: **`<extrusion_distance>`** :fontawesome-solid-divide: **`<requested_extrude_distance>`** :fontawesome-solid-arrow-right-long: **`<rotation_distance>`**

    4.5 :fontawesome-solid-xmark: 102mm :fontawesome-solid-divide: 100mm :fontawesome-solid-arrow-right-long: **4.59**

- I replace the **rotation_distance: 4.5** line in the **`printer.cfg`** file with:<br />
  **rotation_distance: 4.59**:

    ``` title="printer.cfg" hl_lines="6"
    [extruder]
	step_pin: PE0
	dir_pin: !PB9
	enable_pin: !PE4
	microsteps: 16
	rotation_distance: 4.59
    ```


<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
