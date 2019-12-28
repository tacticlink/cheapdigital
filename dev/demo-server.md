## Developing/Demo Server

We need to login cloud server as well as local developing/demo server, the mechanism are same by login with SSH terminal from desktop computer. we choose arch linux run in a USB drive. I use a Sandisk Cruze 8GB USB drive.

I follow the tutorials:

http://valleycat.org/linux/arch-usb.html

If you want to install LXDE desktop environment, follow the tutorials: http://ftp.labdoo.org/download/Public/manuals/wiki.lxde.org/en/Installation.html

Install applications refer to the selections of ubuntu linux, select applications whenever you need. I choose unzip,gedit,firefox.

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
	-v $HOME/addons:/mnt/extra-addons \
	-p 8069:8069 \
	--name odooapp \ 
	--link odoodb:db \
	-t odoo:11.0

Final step, open your web browser, access odoo with

http://localhost:8069
