# 非常非常低的功耗

> 原文：<https://hackaday.com/2016/02/05/very-very-low-power-consumption/>

在这一点上，我们离一个充满壁瘤的世界还很远，你的消费电子产品的默认电源要么是 microUSB 电缆，要么是锂电池。USB 端口无处不在，锂电池拥有足够的电力，这些设备可以工作很长时间。

USB 设备很常见，电池对于大多数设备来说已经足够好了，不是所有的设备。仍然有一个利基市场&需要极长的电池寿命，而接入市电是不切实际的。想想烟雾探测器和安全系统。这些设备的电源是如何工作的？在最近的一份 TI 应用笔记中，TI 展示了他们的超低功耗微控制器[，它带有一个运动检测器，使用标准硬币电池](http://www.ti.com/tool/tida-00489?DCMP=TIDA00489&HQS=sys-ind-ba-TIDA00489Email-adh-rd-null-wwe&sp_rid_pod4=MTE1NzI4MTUxMTgzS0&sp_mid_pod4=50483164&detailID=22265120&spMailingID=50483164&spUserID=MTE1NzI4MTUxMTgzS0&spJobID=842317024&spReportId=ODQyMzE3MDI0S0)可以运行十年。这是每隔几年就会出现的一个小小的工程奇迹，让我们惊讶几分钟，然后几年后就成了意料之中的事情。

在设计使用多年的电池供电设备时，人们首先应该想到的是电池的自放电。十年来，你都不会让一台电池供电的设备配备 AA 电池；Energizer AA 电池的保质期仅为 10 年。再加上几纳安的损耗，你就能幸运地活到 2020 年。不同的是，这是一个 CR2032 锂离子硬币电池。[看看其中一个电池](http://data.energizer.com/PDFs/cr2032.pdf)的数据表，它们可以轻松地在架子上放置 10 年，而剩余 90%的额定容量。

如果设备中有合适的电池，你将需要一个运行在足够低功率下的微控制器，以便在 21 世纪 20 年代中期有用。[这款产品是 CC1310](http://www.ti.com/product/CC1310) ，这是一款极低功耗的 ARM Cortex-M3 和亚 1GHz 发射机，集成在一个封装中。

一旦解决了这个问题，只需在电路板上放置一个传感器(在本例中为 PIR 传感器)和一些偶尔触发中断的模拟位。让微控制器大部分时间处于睡眠模式，这就是你如何获得一个低功耗设备，电池将持续十年。