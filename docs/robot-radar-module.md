# 机器人雷达模块

> 原文：<https://hackaday.com/2018/05/03/robot-radar-module/>

为了他的 Hackaday 奖参赛作品，[Ted Yapo]正在建造一个[机器人雷达模块](https://hackaday.io/project/156535-robot-radar-module)分线板。他的设计使用了来自 [Acconeer AB](https://www.acconeer.com/products) 的 [A111](https://download.acconeer.com/doc/A111%20Datasheet) 60 GHz 脉冲相干雷达(PCR)传感器(新零件警报！) .

A111 是一款低功耗、高精度传感器，非常适合物体检测或手势检测应用。BGA 封装很小——5.5 毫米 x 5.2 毫米，但对黑客来说组装起来并不困难。该传感器在封装中集成了基带、RF 前端和天线，因此您不必担心 RF 布局问题。Acconeer 声称传感器性能不会受到噪音、灰尘、颜色以及直接或间接光线的干扰。感应范围约为 2 米，精确度为+/- 2 毫米。10 台或更多的每台不到 10 美元，这将是增加机器人传感器组件的一个很好的补充。

首先，[Ted]保持他的设计简单小巧——分线板的尺寸仅为 32 mm x 32 mm。雷达传感器本身除了晶体及其负载电容之外不需要任何部件。LDO 负责 A111 所需的 1.8 V 电压。三个 74LVC2T45 芯片将 SPI 数字接口从 1.8 V 转换为 1.8 V 至 5 V 之间的外部逻辑电平。三电平转换芯片可能被一个六通道或八通道转换器取代，例如 TI 的 TXB 系列转换器。对于他的第一个 PCB 迭代，[Ted]预计会遇到一些布局或性能问题，所以如果你对他的设计有任何反馈，请查看他在 [Github](https://github.com/tedyapo/a111-radar) 上的硬件库。

Acconeer 为他们的评估套件提供了一个[入门指南](https://download.acconeer.com/doc/Getting%20Started%20Guide)，其中包括一个详细的 Raspberry-Pi / Raspbian 安装和一个针对黑客的附带视频(在休息后嵌入)。我们热切期待[Ted]在传感器突破方面取得的进展。结合激光雷达 ToF 传感器分线板，如 [MappyDot](https://hackaday.com/2017/08/21/hackaday-prize-entry-mappydot-a-micro-smart-lidar-sensor/) ，这将是对你的机器人的传感能力的巨大补充。

 [https://www.youtube.com/embed/sj9Rxb7WshI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sj9Rxb7WshI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)