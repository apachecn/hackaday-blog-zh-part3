# DIY 智能家居设备意味着不再需要在黑暗中摸索

> 原文：<https://hackaday.com/2016/07/27/diy-smart-home-device-means-no-more-fumbling-in-the-dark/>

智能家居技术正在兴起，但成本或缺乏特定功能可能会让潜在买家犹豫不决。[威士忌探戈酒店]选择使用[树莓 Pi 和蓝牙设备连接](http://www.whiskeytangohotel.com/2016/07/home-automation-via-bluetooth-proximity.html)来设计他们自己的系统。将两种无处不在的技术结合起来，可以在一个人到家时可靠地接近激活方便的功能。

[![Electrical Wiring Diagram](img/4ffd52991f2f6b41d05028daee2a2fc4.png)](https://hackaday.com/wp-content/uploads/2016/07/electrical-wiring-diagram.png)

主要功能是当[威士忌探戈酒店]到家时打开一条 led，以避免在黑暗中摸索灯光，并在设定的时间后关闭它们。Raspberry Pi 和 Bluetooth 加密狗会在一段时间后检测指定的可发现蓝牙设备(在本例中为 iPad)何时进入范围。这将切换 Pi 的 GP10 输出和连接的切换继电器，同时通过 IFTTT 将操作记录到终端和 Google Drive。

 [https://www.youtube.com/embed/DrkR6slSfIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DrkR6slSfIw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Whiskey Tango Hotel]在他们的博客文章[的结尾包含了他们的 Python 代码和构建步骤，如果你开始一个类似的项目，可以帮助你节省一些时间。事实上，树莓 Pi +蓝牙组合可以在许多不同的领域发挥巨大作用——比如为您的汽车音响](http://www.whiskeytangohotel.com/2016/07/home-automation-via-bluetooth-proximity.html)添加[非标准功能。](http://hackaday.com/2014/06/23/raspberry-pi-bluetooth-receiver-for-your-car-stereo/)