#  平價數位化

[為什麼要追逐數位化](https://github.com/tacticlink/cheapdigital/blob/master/basis/pursue-digital_zh.md)

數位化一詞也許是從行銷術語中挪用，指網絡對公司經營活動的影響。數位化的背後是指使用數據，而使用數據意指增強競爭力：通過使用數據，更好了解消費者，而更好了解消費者，進而，根據這種了解，改進產品或服務，通常意味著增強競爭力。由此可見，使用數據需要有數據的來源，應用提供數據，數位化需要應用程式。

本文意在提供一種低價數位化方案。本方案的商業化版在[這裡](https://www.tacticlink.com)

## 開發者桌上型電腦與演示伺服器

- [樹黴派做桌上型電腦](https://github.com/tacticlink/cheapdigital/wiki/pi-desktop)
- [演示伺服器](https://github.com/tacticlink/cheapdigital/blob/master/dev/demo-server_zh.md)

## 通往方案之路

我們的方案建在雲伺服器上，以寬帶網絡連接。 [我的公司是否把應用建在雲上](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud_zh.md)

[如何選擇雲](https://github.com/tacticlink/cheapdigital/blob/master/basis/cloud-guide_zh.md)

[安裝嚮導](https://github.com/tacticlink/cheapdigital/blob/master/dev/towards-applications_zh.md)

# Cheap Digital  

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
