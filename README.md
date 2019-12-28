# Cheap Digital  

[繁體中文](https://github.com/tacticlink/cheapdigital/blob/master/README_zh.md)

We pursue digital,because digital lead the way to data usage, data help us to understand our customers better to increase our competitiveness, so as we can survive. [That is the way data works.](https://github.com/tacticlink/cheapdigital/blob/master/basis/pursue-digital.md)

The intention of this project is to develope a low price Open Source ERP Odoo by yourselves or by limited supports. 

### An Environment for developing

As a developer, you need to work localy before you delivery your work to your customer,we use Pi 3 B+ as our desktop computer.

- [Raspbian as a Desktop](https://github.com/tacticlink/cheapdigital/blob/master/dev/raspbian-desktop.md)
- [Developing/Demo Server](https://github.com/tacticlink/cheapdigital/blob/master/dev/demo-server.md)

### Structure

You need to [decide whether your business go cloud or not.]()

First we need to create a cloud account, requirments vary accourding to different cloud venders,the underlying component for our application is Linux Operating Systems, it is mostly same, the main factor is price. The main cloud vendors is our choices.

The main cloud vendor option list AWS,Google Cloud, Digitalocean, Linode.

After we choose cloud vendor, we need to select 'Ubuntu Linux' as our Operating System,then install docker inside, pull Odoo image, run Odoo container,that is it.
