# 简单有效的车锁干扰器检测器

> 原文：<https://hackaday.com/2017/02/25/simple-and-effective-car-lock-jammer-detector/>

[Andrew Nohawk]注意到，在他的祖国南非，汽车闯入和盗窃事件激增，即使是在光天化日之下。窃贼一直在使用远程干扰器。市面上有商用探测器，但价格高达数百美元。他决定用自己的设备进行实验，用不到一顿普通饭的钱就能快速制造出一个[远程干扰‘探测器’](http://andrewmohawk.com/2017/02/14/remote-jamming-detector-on-the-cheap/)。

根据大多数远程锁工作在 433MHz 的原理，[Nohawk]描述了犯罪分子如何通过按住另一个设备上的锁定按钮来“干扰”频率，希望扭曲或直接中断汽车接收锁门信号。[Nohawk]拿起一个便宜的 433MHz 接收器(捆绑有收发器)，把它扔在一个试验板上，led 连接到 5V 电路上芯片的数据通道，瞧——每当芯片检测到该频率上的活动，LED 就会亮起。如果你看到波段上持续的活动，有可能附近有人在等你，让你的车无人看管。

如果你想更多地了解这些干扰攻击是如何工作的，请查看来自 Hackaday SuperConference 的[【Samy Kamkar 的】演讲。](http://hackaday.com/2016/12/19/samy-kamkar-illustrates-how-to-be-a-hardware-hacker/)

 [https://www.youtube.com/embed/VbZ3cdz4HEA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VbZ3cdz4HEA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



一旦安装在你的车上，你注意到 433MHz 频段被卡住了，随便拿出你的[泰瑟枪手套](http://hackaday.com/2011/10/20/taser-gloves-are-a-bad-idea/)，在你的车周围逗留一会儿，以显示你是认真的。