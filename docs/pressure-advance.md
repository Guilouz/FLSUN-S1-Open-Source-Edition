---
icon: material/car-brake-low-pressure
hide:
  - toc
---

You can define Pressure Advance settings:

- Open **`printer.cfg`** file:

    - On **Mainsail** Web Interface go to **`MACHINE`** tab on the left side.
    - On **Fluidd** Web Interface go to **`Configuration`** icon on the left side.

- Search this line in **`Extruder & Driver Settings`** section and replace the value:

    ``` title="printer.cfg"
    pressure_advance: 0.001
    ```

    The value of **Pressure Advance** can be defined as follows:

    - Value **`=` 0** → Pressure Advance is disabled <br />
    - Value **`<=` 0.002** → Pressure Advance is automatically adjusted by the firmware depending of the speed <br />
    - Value **`>` 0.002** → The defined value is used <br />

- Once done, click on **`SAVE & RESTART`** button at the top right to save the file.

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
