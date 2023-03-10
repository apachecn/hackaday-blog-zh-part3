# 45 岁的谢妮计算器变成了 UDP 服务器

> 原文：<https://hackaday.com/2016/07/15/45-year-old-nixie-calculator-turned-udp-server/>

在这个美丽且有充分证据证明的力量逆向工程壮举中，[Eric Cohen]逆向工程了一个 1971 年的 Singer 计算器，以获得对内部神话般的谢妮电子管的控制。一个不太厉害的黑客会简单地把管子拿出来，放在一个更现代的房子里，[埃里克]把它完好无损地保存了下来。

他甚至不满足于把盒子开膛破肚，把一些现代大脑扔进里面，他窥探到了计算器的内部线路，给它连接了一个树莓派，并否决了计算器的(860 赫兹)总线系统。Pi 在里面，控制着谢妮电子管，他做了我们任何人都会做的事情:建立一个 UDP 服务器，为他的手机编写一个 Android 应用程序，将 ASCII 数据推送到以前的计算器。当然，当它不在默认时钟模式下运行时。

[![nixie-internals](img/5c5e14ab170eab0687d107880e2a3e92.png)](https://hackaday.com/wp-content/uploads/2016/07/nixie-internals.jpg)

所有这些都在他的网站上，在一个[幻灯片演示(PDF)](http://epieye.com/nixie/nixie_calc.pdf) 和视频(嵌入在下面)中得到了非常好的记录。我们的帽子以对细节和精彩文档的惊人关注而著称。

现在，我们为了这样一个场合而保存的 1971 年的 Singer EC1117 计算器在哪里？

 [https://www.youtube.com/embed/mibd44goZ-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mibd44goZ-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

