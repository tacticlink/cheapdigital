## 樹黴派做桌上型電腦

[English](https://github.com/tacticlink/cheapdigital) [繁體中文首頁](https://github.com/tacticlink/cheapdigital/blob/master/README_zh.md)

工作流程是從桌上電腦登錄雲伺服器，在雲伺服器上安裝docker，在docker之上運行Odoo container。所以必須有SSH Terminal，Web Browser。

在工作中使用的桌上型電腦是裝上Raspbian的Raspberry Pi 3 B+，配上顯示器。

若使Raspberry Pi桌上型電腦工作，要滿足下麵條件：

- 一台顯示器，連接顯示器和樹黴派之間的線纜。樹黴派一端是HDMI。
- 樹黴派電源，按照要求，要輸出大於2.5安的USB電源即可。
- 充電寶做不間斷電源（UPS)。

在樹黴派的下載頁上，會看見3個選項，with desktop and sofwares 對於Pi 3 B+來說太重，選image with desktop 或者 image with Rasbian比較好。

#### 選image with desktop 

	# you will need to install applications, for example, install my favorite text exditor 'gedit' 

	$ sudo apt update

	$ sudo apt install gedit


#### 選image with Rasbian Lite

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
	//  add this line to the end, assume pi as user
	pi ALL=(ALL) NOPASSWD:ALL
	//  disable root login
	$ sudo passwd -l root

	### Auto login desktop, in case you boot directely login
	// Edit /etc/lightdm/lightdm.conf
	// Set autologin-user=pi
	$ sudo reboot

	### applications

	# install applications as much as you like.

由此，一台樹黴派Pi 3 B+桌上型電腦可以使用了。
