# 一个适合追踪圣诞老人雪橇的信标？

> 原文：<https://hackaday.com/2016/12/19/a-beacon-suitable-for-tracking-santas-sleigh/>

高空气球正在成为许多大学、学校和黑客空间的流行活动。这些气球可以在平流层中爬升到 40 公里，通常有回收降落伞来帮助有效载荷及其宝贵的数据安全返回地面。但是当你生活在气球大部分时间都可能在海上飞行的地区时，回收有效载荷就成了棘手的事情。来自杜伦大学先进仪器中心的[Paul Clark]和他的团队正在致力于建造一架小型的自主滑翔机——本质上是一个飞行硬盘——从平流层的 30 公里高处航行到主干道附近的降落区。这种系统的一个重要组成部分是帮助找到它的定位信标。他们现在分享了他们设计的"[铱星 9603 信标](https://github.com/PaulZC/Iridium_9603_Beacon)"——一种小型 Arduino 兼容装置，可以通过铱星卫星网络从任何地方传输其位置和其他数据。

信标使用[短脉冲数据服务](https://www.iridium.com/services/details/iridium-sbd)向指定的邮箱发送电子邮件，告知其日期、时间、位置、高度、速度、航向、温度、压力和电池电压。为了做到这一切，它集成了一个 SAMD21G18 M0 处理器；FGPMMOPA6H GPS 模块；MPL3115A2 高度传感器；铱星 9603 短脉冲数据模块+天线和 LTC3225 超级电容器充电器。包括电池和天线在内，整个重量为 72.6 克，非常适合高空气球飞行。整个包裹由三个“AAA”Energizer Ultimate 锂电池供电，应该能够承受飞行中遇到的-56°C。当信标传输数据时，超级电容器需要提供所需的高电流。

该团队已经在美国宇航局哥伦比亚科学气球设施的气球飞行中测试了单个组件，最高可达 35 公里，第一个生产单元将在一个小得多的气球上飞行，大约在圣诞节期间从英国发射。GitHub 存储库包含关于该项目的详细信息，以及 [EagleCAD 硬件](https://github.com/PaulZC/Iridium_9603_Beacon/tree/master/Eagle/V1)文件和 [Arduino 代码](https://github.com/PaulZC/Iridium_9603_Beacon/tree/master/Arduino/Iridium9603Beacon)。现在，只要圣诞老人把这个放在他的雪橇上，[北美防空司令部](http://www.noradsanta.org/)就可以很容易地实时跟踪他的进展。