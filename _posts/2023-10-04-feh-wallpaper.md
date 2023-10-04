---
title: "feh-wallpaper"
date: 2023-10-04
---
To set a wallpaper in i3, you can use a program called `feh`. Here's how you can do it:

1. Install `feh` if it's not already installed. You can do this by running the following command:
   ```
   sudo apt-get install feh
   ```

2. Choose the image you want to set as your wallpaper and remember its file path.

3. Open your i3 configuration file using a text editor. The default location for the configuration file is `~/.config/i3/config`.

4. Add the following line to your i3 configuration file, replacing `<file_path>` with the actual path to your image file:
   ```
   exec --no-startup-id feh --bg-fill <file_path>
   ```

5. Save the changes to your i3 configuration file and exit the text editor.

6. Restart i3 for the changes to take effect. You can do this by pressing `Mod+Shift+R` (by default, `Mod` refers to the `Super` or `Windows` key).

After restarting i3, your chosen image should be set as the wallpaper.
