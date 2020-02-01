---
title: Setting up the Raspberry Pi
---

# Setting up the Raspberry Pi

## Required hardware

![Hardware components]({{ site.url }}/assets/hardware-components.jpg)

The following hardware components are required:

* [Raspberry Pi 4](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/)
* [Raspberry Pi 4 case](https://www.raspberrypi.org/products/raspberry-pi-4-case/)
* [USB-C power supply](https://www.raspberrypi.org/products/type-c-power-supply/)
* 64 GB microSD card
* 128 GB Solid State USB flash drive
* Micro HDMI to HDMI adapter (optional)

## Setup

1. Get the lite-image on the flashcard.
   ```bash
   $ sudo dd bs=1M if=2019-09-26-raspbian-buster-lite.img of=/dev/mmcblk0
   ```
	
   Boot with that image. 
   Careful - sometimes the keyboard pulls a lot of energy and the system will not boot as expected. In this case just boot without a keyboard and plug it in after boot.

1. Login as user `pi` with the default password `raspberry` (`raspberrz` on a german keyboard) to configure the system.

   * Configure the keyboard.
   ```bash
   $ sudo dpkg-reconfigure keyboard-configuration
   ```

   * Reset the password to something secrect.   
   ```bash
   $ passwd
   ```

   * Update the system.
   ```bash
   $ sudo apt update   
   ```

   * Upgrade the system.
   ```bash
   $ sudo apt upgrade
   ```

   * Configure the hostname so it fits your network standard. In our case it is something from the Simpsons.
   ```bash
   $ sudo vi /etc/hostname
   ```

   * Enable ssh.
   ```bash
   $ sudo systemctl enable ssh
   ```

   * Start ssh.
   ```bash
   $ sudo systemctl start ssh
   ```

1. Put your ssh-key on the raspberry pi. 

   * On the local machine
   ```bash
   $ ssh-copy-id pi@frink
   ```
  
   If you are using windows, you need a Putty on your local machine. 
   If you do not know ssh, read about it on the web and just do it.

## More information
* [Raspberry Pi](https://www.raspberrypi.org/)
* [Images for the Raspberry Pi](https://www.raspberrypi.org/downloads/)
* [SSH](https://help.github.com/en/github/authenticating-to-github/about-ssh)
* [Generating a SSH key](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
* [SSH und Windows](https://www.heise.de/tipps-tricks/SSH-unter-Windows-10-nutzen-4224757.html)
