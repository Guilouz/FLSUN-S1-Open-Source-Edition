---
icon: material/map-clock
hide:
  - toc
---

Time Zone is not defined by default, follow these instructions to set it:

- Connect to printer over SSH (see <a href="../ssh-connection">:material-console: SSH Connection</a> section).

- In the SSH command prompt window, enter the following command to check the current time zone:

    ``` title="SSH Command Prompt"
    timedatectl
    ```

- You can change your time zone by entering this command:
  
    ``` title="SSH Command Prompt"
    sudo dpkg-reconfigure tzdata
    ```

- On the page that appears, select your geographic area from the list and press **`Enter`**.

- Then select your time zone in the new list and press **`Enter`**.

- You can then verify that the change has been taken into account by retyping this command:
  
    ``` title="SSH Command Prompt"
    timedatectl
    ```

<br />

**If you like my work, don't hesitate to support me by paying me a 🍺 or a ☕. Thank you 🙂**

<a href="https://ko-fi.com/guilouz" target="_blank"><img width="350" src="../assets/images/ko-fi.png"></a>
