---
title: "fix-steam-debian12"
date: 2023-10-04
---

sudo apt-get update\nsudo apt install libgl1-mesa-dri:i386 libgl1:i386\nsudo apt-get upgrade steam -f\nsudo apt install nvidia-driver-libs:i386
