## 安裝ERP

[English](https://github.com/tacticlink/cheapdigital) [繁體中文首頁](https://github.com/tacticlink/cheapdigital/blob/master/README_zh.md)

應用軟體安裝在雲伺服器上，假定，你已經[決定創建雲計算賬戶](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud_zh.md)，把數字化應用放在雲伺服器上。 [已開立雲賬戶]()。

在Ubuntu Linux上安裝docker有三種方法：

- docker有非常詳細的[安裝步驟文檔](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- Ubuntu apt-get, $ sudo apt-get update && apt-get install docker.io
- [從scripts自動安裝](https://github.com/tacticlink/cheapdigital/blob/master/dev/install-docker.md)。

# 安裝docker之後， pull odoo 11.0 image

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

# Remark: 9876 是對應8069的端口號，用來訪問。
$(PWD)/addons 對應默認目錄下用於放置定制模塊的目錄

# 訪問應用：http://IP:9876
