---
title: "fix-steam-debian12"
layout: post
subtitle: Simple fix for Steam start-up in debian 12
author: m4rv4x
categories: bash
banner:
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: bash
top: 1
sidebar: []
---

sudo apt-get update\nsudo apt install libgl1-mesa-dri:i386 libgl1:i386\nsudo apt-get upgrade steam -f\nsudo apt install nvidia-driver-libs:i386
