# 黑客字典:近场通信(NFC)

> 原文：<https://hackaday.com/2015/10/15/hackaday-dictionary-near-field-communications-nfc/>

你在街角的商店买口香糖。出纳员将购买的东西记入现金出纳机，给你显示金额。你漫不经心地掏出手机，在刷卡机旁挥舞，刷卡机赞赏地发出嘟嘟声。收银员点点头，你走了出来，把口香糖塞到脸上。刚刚发生了什么？您使用近场通信(NFC)在手机和信用卡终端之间发送数据。

NFC 是一种允许两个设备在短距离内交换信息而无需物理接触的标准。这两个设备使用弱磁场进行通信，理论上只有几厘米的范围，所以两个设备必须在物理上靠近，站在附近的人不能拦截或改变信号。

NFC 收发器现在被内置到许多移动设备中，包括 iPhone 和 iWatch，该技术是 Apple Pay 和 Android Pay 等非接触式支付系统的基础。然而，它经历了艰难的演变，从玩具店的好奇到移动世界的主流。这项技术是从旧的射频识别(RFID)系统发展而来的，该系统是为制作电子门禁系统的钥匙而开发的。与 RFID 系统不同，NFC 通信可以双向工作，并且设备可以被写入。

### NFC 起源和基础

第一个使用早期版本 NFC 的设备是 1997 年的《星球大战》玩具，它使用一种早期版本的技术 CommTech 给人物配音。你点击播放器上的芯片，它就会播放声音。这些都是现在颇具收藏价值的[](http://www.commtechguide.com/)。

 [https://www.youtube.com/embed/5stDGP0e05A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5stDGP0e05A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



完整的 NFC 标准于 2002 年被定义为 ISO 标准号 [14443](http://www.iso.org/iso/catalogue_detail.htm?csnumber=50942) 。从那以后，这些标准被由使用它的公司建立的行业组织 [NFC 论坛](http://nfc-forum.org/) 所扩展。

每个对话都有两面性，NFC 也不例外。这种对话有两种模式:被动或主动。在被动模式下，一个设备发射快速交变磁场。这是由另一个设备接收的，它是一个被动设备，只是接收:它不发射磁场。这有效地将两个器件变成了一个气隙变压器，电感导致电流在无源器件的天线中流动。通过改变天线的电阻，无源设备可以调制磁场，向有源设备发回信号。这不需要无源设备中的电池:它从感应电流中获取所需的能量。这就是你会看到的读卡器和交通卡之间的连接类型，比如波士顿的 [查理卡](http://www.mbta.com/fares_and_passes/charlie/) 系统或者伦敦的 [牡蛎卡](https://oyster.tfl.gov.uk/oyster/entry.do) 。

在活动连接中，两个设备都可以发射磁场，它们交替发送和接收磁场。这通常用于两台电脑之间，或两台其他电池供电的设备之间，这些设备需要交换大量数据。

无论哪种方式，该磁场以 13.56MHz 的频率交变，正好在无需许可的工业、科学和医疗(ISM)频段内，这意味着无需许可即可使用。不过，在美国，这种有源设备仍需要 FCC 的批准:你不能在没有获得批准的情况下，就建造自己的有源 NFC 阅读器并出售。

### 数据编码

使用 [幅移键控](https://en.wikipedia.org/wiki/Amplitude-shift_keying) 以 106、212 或 426 千比特每秒的速度发送数据，每个方向使用不同的速度。这样，数据可以同时向两个方向发送，而不会发生冲突。

一旦这两个设备知道了如何相互对话，它们就必须决定说什么。有三种操作模式可供使用:读/写、对等和卡仿真。第一种是当读卡器想从卡上读取数据，然后写回一些内容时使用，比如从交通卡上读取数据，然后写回新存储的票价值。

在对等网络中，两个设备都在发送和接收数据。一个例子是当手机和蓝牙扬声器使用 NFC 来交换关于如何配对蓝牙连接的数据。

在卡仿真中，设备假装成一个哑的、无电的 NFC 卡，即使它是一个功能强大的手机。后者由 iPhone 用于 Apple Pay，因为 iPhone 永远不知道信用卡号码:信用卡号码以加密格式保存在 NFC 芯片本身的安全位置(称为安全元素)。谷歌使用了一种略有不同的方法，称为 [主机卡仿真](https://developer.android.com/guide/topics/connectivity/nfc/hce.html) ，其中卡的详细信息由谷歌加密并保存在云中，而不是在 NFC 芯片上。

 [https://www.youtube.com/embed/qp5il7yhM4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qp5il7yhM4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 如何使用 NFC

正如我之前提到的，你的手机可能已经内置了 NFC 设备。不幸的是，访问它比你想象的要难，因为一些制造商不允许你进行硬件级的访问。Android 提供了最好的支持，允许你在包含 NFC 的设备上通过 Android SDK 进行基本操作，如读取[【NDEF】标签](http://developer.android.com/guide/topics/connectivity/nfc/nfc.html)；或更高级的操作，如 [通过 NFC 连接发送大文件](https://developer.android.com/training/beam-files/send-files.html) 。然而，苹果手机不太合作，因为苹果在当前版本的 SDK 中不提供 NFC 功能。实际上，只有苹果应用程序(如他们自己的 ApplePay 系统)才能访问 NFC 系统。这是否会在 iOS 操作系统的未来版本中继续存在还有待观察，但我不会屏住呼吸:当前的 iOS 9.1 测试版不包括这一点。另外，目前苹果设备上的 NFC 芯片似乎只能 [作为被动设备](http://flomio.com/2014/10/apple-pay-makes-nfc-relevant/) (类似于 NFC 门禁卡)，这意味着它本身无法读取其他被动 NFC 卡和设备。

 [https://www.youtube.com/embed/bp2g9F7ousY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bp2g9F7ousY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果你想真正进入 NFC 的技术领域，你需要拿起一个 NFC 开发工具包。 [Adafruit 提供了一个漂亮的 NFC 分线板](http://www.adafruit.com/products/364) ，可以使用[lib NFC](http://nfc-tools.org/index.php?title=Libnfc)库轻松连接到树莓派 或其他类型的计算机。这将处理无线电信号的编码/解码，同时仍然允许您四处查看。其他开发套件由手机和其他设备使用的芯片制造商提供，包括 [德州仪器](http://www.ti.com/lsds/ti/wireless_connectivity/nfc_rfid/tools_software.page#kits)[恩智浦](http://www.em.avnet.com/en-us/design/drc/Pages/NXP-NFC-Development-Kits.aspx) 等。

获得 NFC 卡的一个有趣方式来自 Moo，他们现在提供配备 NFC 功能的名片。他们称这个想法为 Paper+，并有一些[有趣的想法。这些卡片比普通的卡片更贵(20 张 30 美元)，但是对他们来说有很大的吸引力…](http://www.moo.com/us/products/nfc/paper-plus.html)

![nfc-card](img/d4077e1da29427e6a3b60d0ca98b3fd8.png)

上图: [NFC 查理卡曝光，来自 Adafruit](https://learn.adafruit.com/assets/1017) CC-BY-SA