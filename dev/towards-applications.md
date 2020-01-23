## Road to Applications

[English Home](https://github.com/tacticlink/cheapdigital/blob/master/README_en.md)

We will install applications to a cloud server, first we install docker onto a Ubuntu Linux, then deploy application container up on it. 

Assuming, you have [decided to use a cloud service](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud.md) and [open a cloud account](),

To install docker on Ubuntu Linux server follow the tutorial from docker documentation, or [install docker by scrips](https://github.com/tacticlink/cheapdigital/blob/master/dev/install-docker.md).

	# After docker instllation, pull odoo image

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
