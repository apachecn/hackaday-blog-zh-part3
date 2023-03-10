# 修复你的廉价 NRF24L01+ PA/LNA 模块的可怕范围

> 原文：<https://hackaday.com/2016/05/31/fixing-the-terrible-range-of-your-cheap-nrf24l01-palna-module/>

nRF24L01+ PA/LNA 模块规格在纸面上看起来很棒。在中国，各种廉价来源的小型封装中的无线通信距离可达 1000 米？各种开源项目已经完成的软件连接的艰苦工作？听起来很棒！但是如果你想买并且得到*也许* 1%的范围，不要担心，因为[感谢这些明确的方向，他们可以固定](http://blog.blackoise.de/2016/02/fixing-your-cheap-nrf24l01-palna-module/)。

[Oitzu]通过提供更好的功率、控制噪声、增加屏蔽和小心选择正确的通道，从他的廉价单元获得了更好的性能。他声称,“通过[这些]修改，我在模块外获得了大约 1000 米的自由视线。在一个视线不自由的森林里，我测量了大约 270 米，但这可能不是最大的可能范围。我需要进一步测试。”

经过修改的 nRF24L01+ PA/LNA 模块和 [MySensors](https://www.mysensors.org/) 软件框架被用于我们最近报道的【Oitzu】的另一个项目:他的[太阳能联网鸟舍](http://hackaday.com/2016/05/20/making-solar-powered-networked-birdhouses-putting-them-in-the-middle-of-the-woods/)，在那里他们处理将相机图像传输到树莓 Pi，以便稍后通过移动网络上传。他能够在树林中获得前面提到的 270 米，但在做简单的修改之前，甚至不到十分之一。