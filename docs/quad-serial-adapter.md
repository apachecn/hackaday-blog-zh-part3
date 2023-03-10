# 四路串行适配器

> 原文：<https://hackaday.com/2016/07/22/quad-serial-adapter/>

尽管齐心协力要消灭它们，串行端口仍然存在，尤其是在嵌入式系统中。诚然，目前大多数设备都以 USB 端口结尾，但仍有许多设备使用 DE-9(尽管这个词很常用，但它不是 DB-9)或 TTL 串行端口。[James Fowkes]厌倦了管理一堆 USB 转串行适配器，所以他决定构建自己的 [FT4232 分线板](https://hackaday.io/project/12736-ft4232-quad-serial-breakout)，它将通过 USB 连接提供四个串行端口。

该小型板的每个端口都有发射和接收 led，USB 端口上有 EMI 和 ESD 保护。端口都是 TTL 串行，为现代黑客服务，3.3V 引脚可以承受 5V 电压。

这是一件不难做到的事情，但是非常方便。将所有这些都放在一个经过深思熟虑的板上，可以节省时间。

如果你渴望旧的并行端口，FTDI 设备可以做一个[位爆炸模式](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)。如果你真的担心保护你的 USB 端口，你可以考虑使用[电流隔离](http://hackaday.com/2014/04/27/galvanic-isolated-ftdi-saves-your-computer/)。