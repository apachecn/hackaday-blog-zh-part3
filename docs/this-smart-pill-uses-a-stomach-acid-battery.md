# 这种智能药丸使用胃酸电池

> 原文：<https://hackaday.com/2018/07/07/this-smart-pill-uses-a-stomach-acid-battery/>

[科特·怀特]正在研制一种智能药丸，它的铜锌电池将利用他自己的胃酸作为电解液。这并不是一个不寻常的想法，麻省理工学院在猪身上测试了类似的方法。这也比使用锂离子电池好，我们在这个 PSA 中提到过[。](https://hackaday.com/2016/12/31/psa-dont-let-kids-eat-lithium-batteries/)

![Smartpill circuit diagram](img/df1630981c984b13d77dc5df93be72c1.png)

Smartpill circuit diagram

他的出发点是一个小型的黑客活动追踪器，带有北欧 nRF51822 ARM Cortex-M0 和蓝牙 LE SoC。几乎所有的东西都被拿走了。电池电极被缝在一个按照活动跟踪器的尺寸切割的塑料网上。三个硬币型超级电容器和一个升压转换器位于电池和 SoC 之间。

他用蓝牙 LE 进行交流，算是吧。BLE 设备不断地传输自己的信息，这就是你在扫描可用设备时看到的。该传输中包括 UUID(通用唯一标识符)和名称(例如“smartpillxyz”)。他把药丸放在那个名字里，让药丸传输数据。这通过最小化药丸的蓝牙无线电打开的时间来节省能量。智能手机应用程序从这些传输中提取数据，而无需连接。

他的目标是监控电压和最大电流。这将告诉他他的胃酸电池是否工作，以及它可以为什么供电。第一次测试将使用回流的胃液，然后他会自己吞下药丸。正如他所说，为什么不呢，“人们吞下和通过各种奇怪的东西都没有问题。”他们可能听起来漫不经心，但从他的 hackaday.io 页面来看，他正在做功课。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)