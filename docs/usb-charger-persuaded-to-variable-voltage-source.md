# USB 充电器被骗入可变电压源

> 原文：<https://hackaday.com/2017/06/02/usb-charger-persuaded-to-variable-voltage-source/>

USB 充电器无处不在，每个黑客都有责任将这种常见的设备发挥到极致。[Septillion]和[Hugatry]已经想出了一个黑客操纵 USB 充电器成为一个可变电压源。他们的项目 [QC2Control](https://github.com/septillion-git/QC2Control) 与采用[快速充电 2.0](https://www.qualcomm.com/news/onq/2015/06/30/qualcomm-quick-charge-20-technology-explained) 技术的充电器一起工作，该技术包括壁疣和电源组。

高通的快速充电旨在通过微型 USB 连接器提供高达 24 瓦的功率，以减少兼容设备的充电时间。它要求充电器和终端设备都具有兼容的电源管理芯片，以便它们可以协商电压限制周期。

在他们的项目中，[Septillion]和[Hugatry]使用 3.3 V Arduino Pro Mini，通过由几个电阻和二极管组成的小电路与有问题的充电器对话。当 QC2.0 器件检测到通过 D+和 D-线路传输的预定义电压电平(由 Arduino 和分压器设置)时，它会输出 5 V、9 V 和 12 V 的电压。代码提供函数调用来简化电源的控制。下面的视频展示了黑客的行动。

快速充电已经存在一段时间了，你可以从 TPS61088 (PDF)的[参考设计中深入了解内部工作的细节以及兼容电源的设计。](http://www.ti.com/lit/ug/tidu917/tidu917.pdf)[快速充电技术的专利](http://patentimages.storage.googleapis.com/pdfs/US20140122909.pdf) (PDF)对好奇者来说有更多的细节。

[类似的技术](http://hackaday.com/2017/03/04/unlocking-12v-quick-charge-on-a-usb-power-bank/)在过去已经被使用过，对于那些正在寻找可配置电源的人来说将会证明是有用的。这是给 MacGyver 粉丝的。

 [https://www.youtube.com/embed/MldONoCgr20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MldONoCgr20?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

