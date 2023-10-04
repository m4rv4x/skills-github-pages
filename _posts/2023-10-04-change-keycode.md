---
title: "change-keycode"
date: 2023-10-04
---
To replace keycode 180 with keycode 9 in Debian 12, you can follow these steps:

1. Open a terminal.
2. Run the following command to edit the `evdev` file:
   ```
   sudo nano /usr/share/X11/xkb/keycodes/evdev
   ```
3. In the `evdev` file, locate the line that contains `180` and change it to `9`.
4. Save the file by pressing `Ctrl + O`, then press `Enter` to confirm the filename.
5. Exit the text editor by pressing `Ctrl + X`.
6. Restart your system for the changes to take effect.

After restarting, the keycode 180 should be replaced with keycode 9 in Debian 12.
