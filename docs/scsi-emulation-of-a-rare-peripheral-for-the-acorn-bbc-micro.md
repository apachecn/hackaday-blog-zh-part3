# Acorn BBC Micro 的一个罕见外设的 SCSI 仿真

> 原文：<https://hackaday.com/2017/01/11/scsi-emulation-of-a-rare-peripheral-for-the-acorn-bbc-micro/>

大容量存储对于那些涉及保存旧计算机硬件的人来说是一个问题。虽然以几十年前的标准来看，今天的存储设备既便宜又庞大，但它们的现代接口超出了大多数老式计算机的能力。大容量存储硬件在几十年的忽视后仍然存在，这可能是不可靠的，而且由于其稀有性，如果工作的话，也是相当昂贵的。

末日审判计划 86 团队面临的这个特殊问题比该领域几乎任何其他团队都要大，因为他们的存储设备是一种特别罕见的飞利浦激光光盘驱动器。他们的解决方案是[beebcsi](http://www.domesday86.com/?page_id=400)，这是一个带有 CPLD 和 AVR 微控制器的小型板，分别为现代 micro-SD 卡提供主机适配器和 SCSI-1 仿真。

![An original BBC Domesday set-up. Regregex [CC BY 3.0], via Wikimedia Commons.](img/e5eefc4ad8c51abda995ec8d4aa1d231.png)

一个原始的 BBC 末日调教。Regregex [CC BY 3.0]，通过[维基共享](https://commons.wikimedia.org/wiki/File:VCF_2010_Domesday_tray_open.jpg)。1986 年是《末日审判书》出版 900 周年，这本书是 1086 年由英格兰诺曼国王征服者威廉委托对他的新王国进行的调查和盘点。1986 年纪念这一事件的方式之一是 [BBC 末日审判项目](https://en.wikipedia.org/wiki/BBC_Domesday_Project)，这是 BBC、包括 Acorn 和飞利浦在内的几家技术公司以及来自公众和英国学校系统的大量志愿者之间的合作。收集了全国各地的图片、视频和文本，并用一个不太超文本的界面将它们编辑到一套激光只读存储器上。该系统需要基于 6502 的 BBC Micro 的升级主版本、SCSI 接口和由 Philips 单独为该项目制造的特殊激光盘播放器模型。硬件昂贵、稀有、不可靠，因此很少有贡献者会看到它的运行，它逐渐淡出人们的视野，成为数字档案工作者的名人。

这些年来，这个项目有过几次复活，包括 BBC 自己制作的一个[，你可以在网上浏览](http://www.bbc.co.uk/history/domesday)。这个项目与其他项目的不同之处在于，它尽可能在原始硬件和原始 BBC 微界面上呈现最初打算观看的末日审判体验。2016 年 BBC Master systems 等很多原厂零件相对容易采购，但专用激光视盘播放器肯定不行。这块板取代了链条中不可能的一环，应该让他们不仅仅在屏幕上展示 1986 年的信息。

如果你想看 BBC 末日审判项目的原创系统，你可以在布莱奇利公园的国家计算机博物馆找到一个。与此同时，我们已经推出了与此相同的另一款外设，[小型 USB 转正交鼠标仿真器](http://hackaday.com/2016/10/22/hook-any-mouse-to-an-acorn/)。