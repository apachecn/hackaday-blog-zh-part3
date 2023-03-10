# 利用廉价 USB 集线器进行生物认证

> 原文：<https://hackaday.com/2017/12/07/biometric-authentication-with-a-cheap-usb-hub/>

公平地说，指纹不一定是设备认证的最佳想法，毕竟，它们无处不在。但是在某些情况下，比如一个设备从不离开你的家，指纹是一种加速重复登录的有吸引力的方法。不幸的是，指纹扫描仪还不是普遍存在的硬件。例如，我们对未来的树莓派顶部安装指纹扫描仪不抱太大希望。

为了寻找一种廉价的方式来为他的设备添加指纹扫描功能，[Nicholas]想出了一个聪明的解决方案，不仅便宜，而且多功能。[通过将一个廉价的 USB 集线器与一个指纹扫描仪结合起来，他能够以大约 5 美元的价格组装一个生物识别 USB 集线器，指纹扫描仪原本是 Thinkpad 笔记本电脑的替代部件。](https://adventures-in-tech.blogspot.com/2017/12/diy-lefty-usb-hub-with-fingerprint.html)

[![](img/dcf4702057f0f71b87acdee87d2f1f16.png)](https://hackaday.com/wp-content/uploads/2017/12/fingerhub_detail1.jpg) 买了 Thinkpad 指纹扫描仪后，他想确保它能作为标准 USB 设备被电脑检测到。扫描仪上的连接器和引脚不是标准的，所以他必须刮掉带状电缆的塑料涂层，并用万用表进行一些探测，以找出什么去了哪里。幸运的是，一旦他找到了地线，其余连接的顺序与普通 USB 没有变化。

当连接到他的 Ubuntu 机器时，Thinkpad 扫描仪作为“意法半导体指纹读取器”出现，并可以配置 libpam-fprintd。

现在已经知道了管脚输出和软件配置，剩下的就是把它集成到 USB 集线器中。集线器的一个端口被移除并填充了热熔胶，指纹扫描仪连接到了它的位置。然后在轮毂上切了一个洞，扫描仪就可以从里面出来了。[Nicholas]提到他的 Dremel 目前被租借给了别人，并说他可能会尝试清理箱子，当他拿回它时会稍微开放一些。

[![](img/c0e21642a61c25a0e9860a16857fb5cf.png)](https://hackaday.com/wp-content/uploads/2017/12/fingerhub_detail2.jpg)

[Nicholas]实际上是受到了[的启发，基于他不久前读到的一个黑客帖子来处理这个项目的，所以这个项目真的回到了原点。](https://hackaday.com/2016/01/29/fingerprint-scanner-for-laptop-and-raspberry-pi-or-giving-the-finger-to-your-computer/)[如果你想了解更多关于指纹扫描](https://hackaday.com/2017/04/27/fundamentals-of-fingerprint-scanning/)和正在开发的用于改进它的[技术](https://hackaday.com/2017/09/04/raspireader-an-open-source-fingerprint-reader/)，我们已经为你准备了一些精彩的文章。