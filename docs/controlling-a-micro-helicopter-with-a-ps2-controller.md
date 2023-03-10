# 用 PS2 控制器控制微型直升机

> 原文：<https://hackaday.com/2017/07/24/controlling-a-micro-helicopter-with-a-ps2-controller/>

司马 S107G 是微型直升机市场的一个值得尊敬的坚定支持者。S107G 价格实惠、功能强大且无处不在，它依靠红外线接收控制信号。受到他人先前工作的鼓舞， [[Robert]开始用 Playstation 2 控制器控制他的。](https://www.xarg.org/2017/07/operate-a-syma-s107g-remote-control-helicopter-with-an-arduino/)

在这个项目中，[Robert]可以说是站在巨人的肩膀上——我们以前见过其他人对 S107G 的通信协议进行逆向工程。【罗伯特】联合其他几个人的努力，了解如何向直升机发送命令，包括使用两个独立的通道同时控制两个。

有了必要的协议知识，接下来的事情就是用 9 伏电源将 3 个 led 串联起来，通过连接到计算机的 Arduino 进行切换。电脑上运行的 Javascript 应用程序读取 Playstation 2 控制器的状态，并通过串行接口将其发送到 Arduino，Arduino 会使 led 闪烁。

这不是为你的遥控玩具构建新控制器的最简洁、最轻量级的方式，但它确实展示了通过结合现代硬件和软件工具，一个人可以在一个周末内快速完成一个项目。此外，在一个已经在世界各地试验过的平台上，这是一次很好的学习体验。