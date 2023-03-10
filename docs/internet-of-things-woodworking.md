# 物联网木工

> 原文：<https://hackaday.com/2016/08/31/internet-of-things-woodworking/>

木工是制造夹具的艺术。即使我们有联网的烤面包机、恒温器、汽车和咖啡机，物联网还没有真正出现在木工车间。然而，这种情况正在改变，本·布兰特的物联网盒子展示了连接互联网的廉价电脑到底能做什么。他已经完全自动化了制造箱形接头的过程，所有这一切都是在步进电机和树莓派的帮助下完成的。

[Ben]的电子盒接头夹具的灵感主要来自[Matthias Wandel]的神奇的[螺旋推进盒接头夹具](https://www.youtube.com/watch?v=yuFHurrWswQ)。[Matthias]build 已经成为现代木工车间的“必须制造”夹具之一，它使用木制齿轮来推动托架和原料穿过锯片的锯缝。它的工作非常奇妙，但要正确使用这个手动版本，你需要事先做一些数学计算，在最坏的情况下，在带锯上切割另一个齿轮。

[Ben]的电子盒连接夹具不使用齿轮来沿着螺纹杆移动一块坯料。毕竟，步进电机很便宜，用一个树莓 Pi，一个步进电机驱动器，几个限位开关和几个 led，[Ben]建立了一个互联网支持的箱形接头夹具，能够创建完美的接头。

该构建使用 Raspberry Pi 3 和 Windows IoT 核心来提供一个网页，其中存储了不同的 box joint 配置文件。通过将工件与刀片对齐并按下 start(开始),这种电子盒接头夹具会自动将支架推进到下一个需要的切割位置。所有[本]需要做的就是观察红色和绿色的发光二极管，然后来回推动雪橇。

你可以看看下面[本]的视频。谢谢[迈克尔]的提示。

 [https://www.youtube.com/embed/399oHwYuAG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/399oHwYuAG8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

