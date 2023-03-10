# 纯模块旨在使原型制作更容易

> 原文：<https://hackaday.com/2016/12/25/pure-modules-aim-to-make-prototyping-easier/>

[Sashi]的[纯模块系统](https://hackaday.io/project/12808-pure-modules)希望您的下一个无线微控制器和传感器模块项目使用卡边连接器组装在一起。但它远不止于此——PURE 是一个完整的无线小工具开发生态系统。在完整性和模块化之间取得平衡是非常困难的；一根电线可以传输任何可以想象的电子信号，但是仅仅给某人一堆电线就给了他们一个陡峭的学习曲线。PURE 是另一个极端:一切都是特定的。

到目前为止，系统中有两种微控制器可供选择，nRF52 系列和 TI 的 CC2650。这两款都运行 Contiki OS 操作系统，所以你选择哪一款并不重要。有线数据全部通过 I2C 传输，并通过前面提到的卡边连接器连接起来。在无线方面，数据传输通过 [MQTT 代理](http://hackaday.com/2016/05/09/minimal-mqtt-building-a-broker/)处理，使用 [MQTT-sn](http://mqtt.org/2013/12/mqtt-for-sensor-networks-mqtt-sn) 变体，更适合小型无线电设备。在协议层，一切都使用[协议缓冲区](https://developers.google.com/protocol-buffers/)，这是谷歌为数据增加一些结构的最新想法。

[![modules_in_arduino](img/b8024fc331c4b38b29ef432b599a3dbd.png)](https://hackaday.com/wp-content/uploads/2016/12/modules_in_arduino.jpg) 这一切意味着，让代码、设备、连接 WiFi 的计算机和服务协同工作应该非常容易。除了 Hackaday.io 上提供的概述，GitHub 上还有[硬件](https://github.com/PureEngineering/PUREmodules)和[软件](https://github.com/PureEngineering/contiki/tree/master/platform/puremodules)库，而且【Sashi】甚至还整合了一个[指令库](http://www.instructables.com/id/PUREmodules-How-to-Make-Your-Own-Module/)来让你开始制作自己的模块。目前它也在 Kickstarter 上发布，所以如果你不想自己动手的话，可以去看看。

PURE 在每一步都使用了当前的开源和可互操作技术，整合成一个看起来像是经过深思熟虑的系统。像这样的东西会帮助你逃离成为我们现代黑客场景特征的[连接器动物园](http://hackaday.com/2016/11/09/my-life-in-the-connector-zoo/)？我们不知道，但它看起来像一个完全合理的[第十五标准](https://xkcd.com/927/)。

 [https://www.youtube.com/embed/7Rj3Zab86_k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7Rj3Zab86_k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

