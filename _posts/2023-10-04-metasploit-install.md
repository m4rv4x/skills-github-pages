---
title: "metasploit-install"
layout: post
subtitle: Install metasploit framework on debian 12
author: m4rv4x
categories: bash
banner:
  opacity: 0.618
  background: "#000"
  height: "100vh"
  min_height: "38vh"
  heading_style: "font-size: 4.25em; font-weight: bold; text-decoration: underline"
  subheading_style: "color: gold"
tags: bash hacking
top: 1
sidebar: []
---
To install Metasploit on Debian 12, you can follow these steps:

1. Update the package lists and upgrade the system:
   ```
   sudo apt update
   sudo apt upgrade
   ```

2. Install the required dependencies:
   ```
   sudo apt install curl gnupg2
   ```

3. Import the Metasploit repository GPG key:
   ```
   curl https://apt.metasploit.com/metasploit-framework.gpg.key | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/metasploit-framework.gpg
   ```

4. Add the Metasploit repository to the sources list:
   ```
   echo "deb [arch=amd64] https://apt.metasploit.com/ bookworm main" | sudo tee /etc/apt/sources.list.d/metasploit-framework.list
   ```

5. Update the package lists again:
   ```
   sudo apt update
   ```

6. Install Metasploit:
   ```
   sudo apt install metasploit-framework
   ```

7. After the installation is complete, you can start Metasploit by running:
   ```
   msfconsole
   ```

Please note that Metasploit is a powerful tool and should only be used for ethical purposes, such as penetration testing on authorized systems.
