---
title: "bt-keymap-script"
date: 2023-10-04
---
To start a custom keymap when using your Bluetooth keyboard on Debian 12, you can follow these steps:

1. Identify the device ID of your Bluetooth keyboard by running the following command:
   ```
   $ xinput list
   ```

   Look for the entry corresponding to your Bluetooth keyboard. Note down the device ID.

2. Create a new udev rule to apply the custom keymap when the Bluetooth keyboard is connected. Run the following command to create a new rule file:
   ```
   $ sudo nano /etc/udev/rules.d/99-bluetooth-keyboard.rules
   ```

   In the editor, add the following line:
   ```
   ACTION=="add", SUBSYSTEM=="input", ATTRS{idVendor}=="YOUR_VENDOR_ID", ATTRS{idProduct}=="YOUR_PRODUCT_ID", RUN+="/path/to/your/custom-keymap.sh"
   ```

   Replace `YOUR_VENDOR_ID` and `YOUR_PRODUCT_ID` with the vendor and product IDs of your Bluetooth keyboard. Also, replace `/path/to/your/custom-keymap.sh` with the actual path to your custom keymap script.

3. Save the file and exit the editor.

4. Create the custom keymap script mentioned in the udev rule. Run the following command to create the script file:
   ```
   $ sudo nano /path/to/your/custom-keymap.sh
   ```

   In the editor, add the commands to set up your custom keymap. For example, if you want to use the "colemak" keymap, you can use the following command:
   ```
   setxkbmap -layout us -variant colemak
   ```

   Customize the script according to your desired keymap configuration.

5. Save the file and exit the editor.

6. Make the script executable by running the following command:
   ```
   $ sudo chmod +x /path/to/your/custom-keymap.sh
   ```

7. Reload the udev rules by running the following command:
   ```
   $ sudo udevadm control --reload-rules
   ```

8. Disconnect and reconnect your Bluetooth keyboard.

Your custom keymap should now be applied automatically whenever you connect your Bluetooth keyboard to your Debian 12 system.
