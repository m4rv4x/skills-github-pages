---
title: "grub-update"
layout: post
subtitle: Update your GRUB to boot correctly
author: m4rv4x
categories: bash
banner:
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: bash config
top: 1
sidebar: []
---

Yes, there is a package called `os-prober` that can help you configure GRUB to include your Windows 10 partition for UEFI boot. You can install it by running the following command:

```
sudo apt install os-prober
```

After installing `os-prober`, you can update GRUB to include the Windows 10 partition by running:

```
sudo update-grub
```

This will scan your system for other operating systems and add them to the GRUB boot menu.
