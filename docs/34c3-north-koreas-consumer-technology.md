# 34C3:朝鲜的消费技术

> 原文：<https://hackaday.com/2017/12/30/34c3-north-koreas-consumer-technology/>

[Will Scott]和[Gabe Edwards]在他们的演讲[朝鲜消费技术](https://media.ccc.de/v/34c3-9279-dprk_consumer_technology)中，对 34C3 消费计算技术的现状进行了一些阐述。两人还创建了一个网站作为这些信息的交换中心——包括在 koreaComputerCenter.org[的智能手机操作系统映像。](http://www.koreacomputercenter.org/)

对于朝鲜公民能获得什么样的技术，还不是很清楚。我们已经看到了[红星操作系统](https://en.wikipedia.org/wiki/Red_Star_OS)，它是一种基于 Linux 的类似 Mac 的操作系统，用在基于 PC 的台式机上。但是智能手机等其他系统呢？

[威尔]和[加布]发现，朝鲜的手机通常由中国公司制造，运行定制版的安卓操作系统。手机硬件很常见——在朝鲜以平壤 2407 出售的手机在印度也以 Genie v5 出售。如果你能得到这个精灵，你就能在这个硬件上运行韩国版的 Android 操作系统。

![](img/140b71c4cd4dcc3c73bbba3f5f0b3003.png)

North Korean App Store

应用商店也不一样。朝鲜安卓没有软件应用商店。要购买应用程序，用户需要去实体店，从目录中挑选。商店老板然后通过电缆将应用程序下载到客户的手机上。

朝鲜非常重视教育。手机和平板电脑包括许多教科书的 pdf 文件。您可以学习 Java、Linux 和其他主题。PDF 文件被加密并锁定在特定的设备上。[Will]和[Gabe]发现 ezPDF Android 使用的一个公共库被更改了。朝鲜的某个人实际上已经进入并修改了二进制文件，在图书馆的文件处理代码中加入了解密算法。加密系统本身并不难破解——一个 512 字节的 XOR pad 被硬编码在库的末尾。设备 MAC 地址用于计算 XOR pad 中的偏移量并解密文件。

[威尔]和[加布]只是触及了现有数据的表面，在 koreaComputerCenter.org 还有更多可以发现。想进一步了解红星 OS？查看[出此条](https://hackaday.com/2015/01/10/messing-around-with-naenara-north-koreas-web-browser/)！

[https://media.ccc.de/v/34c3-9279-dprk_consumer_technology/oembed](https://media.ccc.de/v/34c3-9279-dprk_consumer_technology/oembed)