---
title: Setting up the Raspberry Pi
---

# Setting up the Raspberry Pi

![Hardware components]({{ site.url }}/assets/hardware-components.jpg)

## Setup

Read up a little on the following pages:
[Raspberry Pi](https://www.raspberrypi.org/)
[Images](https://www.raspberrypi.org/downloads/)
[]()
[SSH und Windows](https://www.heise.de/tipps-tricks/SSH-unter-Windows-10-nutzen-4224757.html)

* Get the lite-image on the flashcard.
  $ sudo dd bs=1M if=2019-09-26-raspbian-buster-lite.img of=/dev/mmcblk0
	
Boot with that image. 
Careful - sometimes the keyboard pulls a lot of energy and the system will not boot as expected. In this case just boot without a keyboard and plug it in after boot.

* Login with “pi” und “raspberrz” (english keyboard) and configure the system.

** Configure the keyboard.
  $ sudo dpkg-reconfigure keyboard-configuration

** Reset the password to something secrect.   
  $ passwd

** Update the system.
  $ sudo apt update

** Upgrade the system.
  $ sudo apt upgrade

** Configure the hostname so it fits your network standard. In our case it is something from the Simpsons.
  $ sudo vi /etc/hostname

** Enable ssh.
  $ sudo systemctl enable ssh

** Start ssh.
  $ sudo systemctl start ssh

** Put your ssh-key on the raspberry pi. On the local machine
  $ ssh-copy-id pi@frink
  
If you are using windows, you need a Putty on your local machine. 
If you do not know ssh, read about it on the web and just do it.
