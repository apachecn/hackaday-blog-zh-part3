# 作为硬件黑客终端的袖珍芯片

> 原文：<https://hackaday.com/2017/09/08/pocketchip-as-a-hardware-hackers-terminal/>

如今，会议可能是一个棘手的地方——尤其是硬件和黑客会议。如果你不是黑客，那么你可以肯定你的设备正在被探测、侦测，甚至可能被黑客攻击。这当然不是带你珍贵的笔记本电脑的地方。此外，随着时间的推移，你的脚开始疼痛，普通笔记本电脑开始感觉更大更重。你需要的是一次性笔记本电脑——轻便、便宜，而且不介意被黑客攻击。[dalmoz]写了一篇简短扼要的教程，介绍如何在 UART 连接方面将 PocketCHIP 作为硬件黑客最好的朋友。它还可以方便地用作项目的独立串行监视器，而不必专门使用 USB 端口和屏幕。

[PocketCHIP](https://getchip.com/pages/pocketchip) 是 C.H.I.P .微型计算机的坞站，在一个轻便的模塑外壳中添加了 LED 背光触摸屏显示器、QWERTY 键盘和 LiPo 电池。花 70 美元，你就可以得到 1 GHz ARM v7 处理器、512MB 内存、Mali 400 GPU、WiFi 和蓝牙。它很轻，可以通过挂绳槽挂在脖子上。所有 GPIO 引脚都方便地分开，包括 UART 引脚。目前，它在 Kickstarter 的支持者手中，但 Next Thing Co 网站表示将在本月某个时候推出。

在硬件方面，您需要做的只是在 PocketCHIP GPIO 接头上为 TX、RX 和 GND(如果需要，可能是 5 V 和 3 V)添加接头引脚，就万事大吉了。在软件方面，事情同样简单。UART 引脚用于提供对芯片本身的调试访问，需要从内部任务中释放出来。一旦 UART 端口被识别，单个终端命令释放其作为调试接口的状态。之后，使用任何终端仿真器——[ dal moz]推荐 Minicom——就万事俱备了。万一你只有一个 Arduino，dalmoz 贴了一个简单的草图来确保你能让它工作。很棒的黑客技巧，因为这再简单不过了。如果你想了解更多关于芯片项目的信息，可以查看它的[文档](https://docs.getchip.com/chip.html)和 [Github](https://github.com/NextThingCo) 库——它们都是开源的。