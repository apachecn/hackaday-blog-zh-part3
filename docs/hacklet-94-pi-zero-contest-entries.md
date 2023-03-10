# hack let 94–Pi 零竞赛参赛作品

> 原文：<https://hackaday.com/2016/02/06/hacklet-94-pi-zero-contest-entries/>

Hackaday 和 Adafruit 联手推出了[树莓派零点大赛](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)。然而，没有参赛作品，一场伟大的比赛就什么都不是。这是 [Hackaday.io](https://hackaday.io) 社区再次证明他们是世界上最好的。比赛还不到一周，但是截止到本周四晚上，[我们已经有 33 名参赛者了](https://hackaday.io/submissions/adafruitpizerocontest/list)！您应该现在提交您自己的项目想法，以便有机会获得众多奖项之一。本周在 Hacklet 上，我们将看看这些早期进入者中的几个！

[![controller](img/cc1159c70e6e7e8975a7f2f50e0e8649.png)](https://hackaday.io/project/8703) 我们从【usedbytes】和[Zero Entertainment System](https://hackaday.io/project/8703)【usedbytes】多亏了 Raspberry Pi Zero，将整个仿真器塞进了一个经典的任天堂娱乐系统控制面板。Zero Entertainment System 还拥有最初的 NES 做梦也想不到的东西:HDMI 输出。仿真器使用流行的 RetroPie 前端。我们很高兴地说，[usedbytes]知道破解一个真正的任天堂控制器将是亵渎，所以他们从远东抓了一个低成本的 USB 克隆。一些有创意的部件——填充和点到点的布线之后，ZES 准备好与世界见面了！

[![wspr](img/a6ea040ad7e849fff9f5695f7623a103.png)](https://hackaday.io/project/9484) 接下来是【珍妮名单】与[澳洲项目](https://hackaday.io/project/9484)。[Jenny]是来自欧洲的黑客。她希望用零圆周率和澳大利亚通话。“谈话”可能有点过了。澳大利亚项目将使用弱信号传播报告器(WSPR)网络直接从 Pi 的 GPIO 端口传输 RF。所需的只是一个好的滤波器、一个天线和一个巴伦。这种情况下，滤波器是一个 7 极点切比雪夫低通滤波器。该滤波器防止圆周率的谐波填充方波搞乱从 DC 到光的每个频带。[【Jenny】通常将这些滤镜作为套件](http://shop.languagespy.com/collections/frontpage/products/pi-lpf-low-pass-filter-kit-for-the-raspberry-pi)出售，但她专门为 Pi Zero 制作了一个特殊版本。

[![tote0](img/44984d6ee31d1fc5a907340b6a3394c6.png)](https://hackaday.io/project/9065) 【拉多米尔·多皮耶拉斯基】带着[托特零](https://hackaday.io/project/9065)把他标志性的行走机器人带到了圆周率为零的世界。Tote Zero 是一个四足步行机器人，主要由 9 克伺服系统组成。[Radomir 的]定制托特板接口伺服到 Pi 零本身。Pi Zero 为传感器、视觉和高级处理打开了各种大门。原始手提袋上的 Arduino 板很难实现这一点。Tote 是用 Python 编程的，这将使代码快速且易于开发。几天前，Tote Zero 刚刚迈出了它的第一步，因此，随着一个新机器人的诞生，请跟随它吧！

[![ethernetpo](img/ebfdbe85463b2cdb83a8d30abd9063ae.png)](https://hackaday.io/project/9455) 最后我们有【朱利安】与 [PoEPi: Pi 零功耗以太网与 PHY](https://hackaday.io/project/9455) 。Raspberry Pi Zero 是如此之小，以至于人们很容易忘记它需要相当大的功率才能运行。[Julien]为我们提供了一种将 Pi 连接到网络的方法，同时使用以太网供电(PoE)来抛弃 USB 电源。多年来，PoE 一直为 IP 摄像头等设备供电。它已经成为传输能量和数据的标准方式。对于以太网物理接口，[Julien]使用微芯片的 ENC28J60，它有一个方便的 SPI 接口。Linux 已经为这种设备准备了驱动程序，所以这是一件轻而易举的事。该系统的“电源”部分由 LTC4267 PoE 接口芯片提供帮助，该芯片内置开关稳压器。

如果你想看到更多的参赛者参加 Hackaday 和 Adafruit 的圆周率为零竞赛，[请查看提交列表](https://hackaday.io/submissions/adafruitpizerocontest/list)！如果你在那个列表上没有看到你的项目，你甚至不用联系我，[只要把它提交给 Pi 零竞赛](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)！这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！