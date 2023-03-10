# I2c 中继扩展器使用漂亮的卡边连接

> 原文：<https://hackaday.com/2016/05/18/i2c-relay-expander-uses-nifty-card-edge-connection/>

[Andrew Sowa]想要使用 Numato Labs 的现成中继板。该板缺乏合适的计算机接口，这意味着[Andrew]将不得不建立一个，其输入连接器是螺丝端子，这意味着大量的布线。他没有被吓倒，他使用 MCP23017 I/O 端口扩展器创造了 i2c 扩展卡,并采用了一种新颖的卡边设计来与螺丝端子配合，一次性解决了这两个问题。


该板是在 KiCad 中设计的，如果你有兴趣自己创建一个[它的文件在他的 GitHub 库](https://github.com/Junes-PhD/FRM16_Relay_Module_I2C_Controller)中，他的板甚至可以作为[从 OSH Park](https://oshpark.com/shared_projects/YMBXgnZ5) 共享项目获得。我们希望 ENIG 完成是那些螺丝终端连接器的资产。

[Andrew]的电路板与众不同的外形正好与螺丝端子匹配，没有在他的材料清单中添加任何连接器或线路。当然，额外 PCB 表面积的成本和布线成本之间存在权衡，但我们可以看到，对于像他这样需要控制合理数量的继电器板的人来说，布线会失去控制。

这些年来，我们在 Hackaday 展示了 PCB 制造的方方面面。但令人惊讶的是，电路板往往只是电路的基板。值得提醒的是，它也是一个组件，与大多数其他组件不同，它可以赋予您选择的功能，而不必依赖现成的功能。