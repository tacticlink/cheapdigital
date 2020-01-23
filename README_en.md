# Cheap Digital  

[繁體中文](https://github.com/tacticlink/cheapdigital)

We pursue digital,because digital lead the way to data usage, data help us to understand our customers better to increase our competitiveness, so as we can survive. Read more about [Why we pursue digitalization?](https://github.com/tacticlink/cheapdigital/blob/master/basis/pursue-digital.md)

The intention of this project is to develope a low price Open Source ERP Odoo by yourselves. 

## An Environment for developing

As a developer, you need to work localy before you delivery your work to your customer,we use Pi 3 B+ as our desktop computer.

Meanwhile, you need a Demo server as well, to demo/develop what you want to achieve. We select Arch Linux run in a USB Drive.

- [Raspbian as a Desktop](https://github.com/tacticlink/cheapdigital/blob/master/dev/raspbian-desktop.md)
- [Developing/Demo Server](https://github.com/tacticlink/cheapdigital/blob/master/dev/demo-server.md)

## Structure

All applications will be depoyed on a cloud server, that rise questions: what Cloud is? Should I adopt cloud? First of all, you need to [decide whether your business go cloud or not.](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud.md)

First we need to create a cloud account, requirments vary accourding to different cloud venders,the underlying component for our application is Linux Operating Systems, it is mostly same, the main factor is price. The main cloud vendors is our choices.

After we choose cloud vendor, we need to select 'Ubuntu Linux' as our Operating System,then install docker inside, pull Odoo image, run Odoo container,that is it.

[The Cloud Vendor guide](https://github.com/tacticlink/cheapdigital/blob/master/basis/cloud-guide.md)

[The Steps towards to an Odoo application.](https://github.com/tacticlink/cheapdigital/blob/master/dev/towards-applications.md)
