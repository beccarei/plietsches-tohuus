---
title: Setting up the Raspberry Pi
---

# Setting up the Raspberry Pi

![Hardware components]({{ site.url }}/assets/hardware-components.jpg)

Flash with

    $ sudo dd bs=1M if=2019-09-26-raspbian-buster-lite.img of=/dev/mmcblk0

Login with “pi” und “raspberrz” (english keyboard)

    $ sudo dpkg-reconfigure keyboard-configuration

    $ passwd

    $ sudo apt update

    $ sudo apt upgrade

    $ sudo vi /etc/hostname

    $ sudo systemctl enable ssh

    $ sudo systemctl start ssh

On the local machine

    $ ssh-copy-id pi@frink
