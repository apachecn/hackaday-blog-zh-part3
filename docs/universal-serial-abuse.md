# 普遍系列虐待

> 原文：<https://hackaday.com/2016/08/17/universal-serial-abuse/>

很可能大多数黑客读者都知道他们自己的计算机安全，即使他们不是专家。您将对您的机器向外界公开哪些端口、它们运行什么服务有所了解，并且您将知道一堆可能的攻击媒介，即使您可能不知道每一个。

因此，作为这种意识的一部分，你可能会对陌生的 USB 设备保持警惕。如果有人在停车场丢了一个闪存盘，你们中的一个愉快地把它插到笔记本电脑上的几率一点都不高。你的电脑及其操作系统信任 USB 端口，拥有一个 USB 端口就等于拥有了通往王国的钥匙。

我们今天的主题是由[Dominic White]和[Rogan Dawes]提供的 DEF CON talk，标题为" [Universal Serial aBUSe](https://www.sensepost.com/blog/2016/universal-serial-abuse/) "，它详细描述了一个 USB 攻击，其中他们创建了一个无害的 USB 棒，模拟键盘和鼠标，通过 VNC 服务器在 WiFi 网络上共享。这给了攻击者(他可以获得对 USB 端口的瞬时物理访问以安装设备)一种完全绕过所有网络和其他安全措施进入机器的方法。

他们的硬件配备了一个 AVR 和一个 ESP8266，前者用于 USB 和 HID 工作，后者用于完成繁重的工作并提供 WiFi。他们从一个 [Cactus Micro Rev2](https://www.tindie.com/products/AprilBrother/cactus-micro-rev2-arduino-compatible-plus-esp8266/) 开始，但是升级到他们自己的兼容板，使设备更适合作为 USB 棒。硬件和软件文件[都可以在他们的 GitHub 库](https://github.com/sensepost)上找到，软件是 [esp-link](https://github.com/jeelabs/esp-link) 的一个分支。他们深入研究了开发和调试过程的重要细节，他们的文章对任何人来说都是有趣的读物。

在广告下方，你可以看到一段描述此次袭击的视频。知道 USB 端口的防御如此之弱并不令人震惊，但这是一个清醒的时刻，意识到像这样的攻击已经到了什么是可能的境界。

 [https://www.youtube.com/embed/5gMvtUq30fA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5gMvtUq30fA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



USB 安全是我们之前在 Hackaday 讨论过的内容，Shmoocon 和 [DEF CON 讨论过使用设备微控制器的 BadUSB 漏洞。不过，我们最喜欢的解决方案是 USB 杀手](http://hackaday.com/2014/10/05/badusb-means-were-all-screwed/)，这是一种烧坏那些插入停车场 u 盘的人的端口的设备。