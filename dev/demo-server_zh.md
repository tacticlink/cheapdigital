## 演示伺服器

模擬雲伺服器需要一個本地伺服器，同時，演示伺服器兼做開發伺服器用。雲伺服器假設運行Ubuntu Linux與本地伺服器上運行的Arch Linux在安裝了docker之後，命令相同，本地演示/開發伺服器用Arch Linux， 選擇安裝在USB Drive上，使用Sandisk Cruz 8GB USB。

安裝Arch Linux按照如下教程：

http://valleycat.org/linux/arch-usb.html

安裝LXDE桌面按照如下教程：

http://ftp.labdoo.org/download/Public/manuals/wiki.lxde.org/en/Installation.html

參照Ubuntu Linux的選項， 安裝unzip,gedit,firefox.


	# install docker in arch linux

	sudo pacman -Syu #Update mirror list

	sudo pacman -S docker

	# pull odoo 11 docker images

	pull odoo:11.0

	pull postgres:10

	# run odoo 11 docker container

	## run database container

	docker run -d \
	--restart always \
	-e POSTGRES_USER=odoo \
	-e POSTGRES_PASSWORD=odoo \ 
	-e POSTGRES_DB=postgres \
	--name odoodb \
	postgres:10

	## run odoo container

	docker run \ 
	--restart always \
	-v $(PWD)/addons:/mnt/extra-addons \
	-p 9876:8069 \
	--name odooapp \ 
	--link odoodb:db \
	-t odoo:11.0

	# Remark: 9876 is your port number, you can select port number as you like.  

打開瀏覽器，訪問Odoo

	http://localhost:9876
