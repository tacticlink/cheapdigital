## Raspbian as a Desktop

[Home](https://github.com/tacticlink/cheapdigital/blob/master/README.md)

We recommand Linux, Raspbain, as we used in our work, as your desktop. Being a developer, to deliver a cloud server to customer,you need a SSH Terminal,  as well as a web browser for minimum.

First check up your requiment,

- You need a mornitor and a cable betwwen Pi board and the monitor.

- Your Power Supply should meet the Pi specifcation, Pi offcial documents recommand an USB Power Supply > 2.5A. See https://www.raspberrypi.org/documentation/hardware/raspberrypi/power/README.md

- We also use a power bank as UPS, you can choose your preffer brand.

You will find 3 options on Pi's download site, the image with desktop and sofwares are too heavey to run on Pi3 B+, I take the image with desktop and the image with Rasbian only,the upper comes with Raspberry customed desktop only need to install applications, the later you need to install  desktop and applications.

#### If you choose image with desktop

	# you will need to install applications, for example, install my favorite text exditor 'gedit' 

	$ sudo apt update

	$ sudo apt install gedit


#### If you choose image with Rasbian Lite

	# you need to install desktop and applications

	$ sudo apt update

	### Desktop, this is for lxde desktop

	sudo apt-get install --no-install-recommends xserver-xorg
	sudo apt-get install --no-install-recommends xinit
	sudo apt-get install lxde-core lxappearance
	sudo  apt-get install lightdm

	###  sudo no password, you may not want to issue sudo password every time.
	$ sudo passwd  # set root password
	$ su root  # login as root
	$ visudo
	//  add this line to the end
	jon ALL=(ALL) NOPASSWD:ALL
	//  disable root login
	$ sudo passwd -l root

	### Auto login desktop, in case you boot directely login
	// Edit /etc/lightdm/lightdm.conf
	// Set autologin-user=pi
	$ sudo reboot

	### applications

	install applications as much as you like.

Thus a desktop computer ready to use, it includes an SSH Terminal, and a web browser , and a desktop environment whether it is a lxde or Pi customed desktop.
