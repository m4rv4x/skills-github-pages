---
title: "grub-update"
date: 2023-10-04
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
