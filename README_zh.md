#  平價數字化

[English](https://github.com/tacticlink/cheapdigital)

數字化一詞也許是從行銷術語中挪用，指網絡對公司經營活動的影響。數字化的背後是指使用數據，而使用數據意指增強競爭力：通過使用數據，更好了解消費者，而更好了解消費者，進而，根據這種了解，改進產品或服務，通常意味著增強競爭力。由此可見，使用數據需要有數據的來源，應用提供數據，數字化需要應用程式。[為什麼要追逐數字化](https://github.com/tacticlink/cheapdigital/blob/master/basis/pursue-digital_zh.md)

本文意在提供一種低價數字化方案。本方案的商業化版在[這裡](https://www.tacticlink.com)

## 開發者桌上型電腦與演示伺服器

- [樹黴派做桌上型電腦](https://github.com/tacticlink/cheapdigital/blob/master/dev/raspbian-desktop_zh.md)
- [演示伺服器](https://github.com/tacticlink/cheapdigital/blob/master/dev/demo-server_zh.md)

## 通往方案之路

我們的方案建在雲伺服器上，以寬帶網絡連接。 [我的公司是否把應用建在雲上](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud_zh.md)

## Structure

All applications will be depoyed on a cloud server, that rise questions: what Cloud is? Should I adopt cloud? You need to [decide whether your business go cloud or not.](https://github.com/tacticlink/cheapdigital/blob/master/basis/go-cloud.md)

First we need to create a cloud account, requirments vary accourding to different cloud venders,the underlying component for our application is Linux Operating Systems, it is mostly same, the main factor is price. The main cloud vendors is our choices.

The main cloud vendor option list AWS,Google Cloud, Digitalocean, Linode.

After we choose cloud vendor, we need to select 'Ubuntu Linux' as our Operating System,then install docker inside, pull Odoo image, run Odoo container,that is it.

[The Cloud Vendor guide](https://github.com/tacticlink/cheapdigital/blob/master/basis/cloud-guide.md)

[The Steps towards to an Odoo application.](https://github.com/tacticlink/cheapdigital/blob/master/dev/towards-applications.md)
