---
title: "polybar-dark-tray"
layout: post
subtitle: How to set Dark mode tray icons for polybar
author: m4rv4x
categories: i3
banner:
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: bash i3 customization
top: 1
sidebar: []
---

To change the nm-applet icon to a dark theme in polybar, you can follow these steps:

1. Open your polybar configuration file. Usually, it is located at `~/.config/polybar/config`.

2. Find the module section for the nm-applet in the configuration file. It should look something like this:

   ```
   [module/nm-applet]
   type = internal/network
   interface = wlan0
   format-connected = <label-connected>
   format-disconnected = <label-disconnected>
   label-connected = %essid% %ip%
   label-disconnected = Disconnected
   ```

3. Add the `label-connected-foreground` and `label-disconnected-foreground` options to the module section. Set the values to the desired color for the connected and disconnected states. For example:

   ```
   [module/nm-applet]
   type = internal/network
   interface = wlan0
   format-connected = <label-connected>
   format-disconnected = <label-disconnected>
   label-connected = %essid% %ip%
   label-disconnected = Disconnected
   label-connected-foreground = #FFFFFF
   label-disconnected-foreground = #AAAAAA
   ```

   Replace `#FFFFFF` and `#AAAAAA` with the appropriate color codes for your dark theme.

4. Save the configuration file and restart polybar for the changes to take effect.

Now, the nm-applet icon in polybar should be displayed with the dark theme colors you specified.
