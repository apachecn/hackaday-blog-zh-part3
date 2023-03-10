# 监测空气质量，一次一个瞌睡会

> 原文：<https://hackaday.com/2018/05/29/monitoring-air-quality-one-sleepy-meeting-at-a-time/>

对我们这些企业界人士来说，会议室是希望破灭的地方。挤在一个对被邀请者来说太小的空间里，随着最后一次淋浴时间的逐渐增加，房间很快就散发出人体热量和人类的香味。说它不是提高生产率的良方是一种保守的说法。

在经历了太多这种令人昏昏欲睡的情况后，[查尔斯·欧文兰]决定自己动手，为会议制造了这个便携式空气质量测量仪。顶部有一个 OLED 显示屏，内部有传感器，它不仅可以显示温度、湿度和大气压力，还可以显示 CO₂浓度和挥发性有机化合物(VOC)的水平，这些有毒物质有时会从建筑材料、家具装饰和同事等排放出来。

班长量化了他开会时的痛苦，我们确信这为他赢得了同事们的好感。然而，对我们来说，我们觉得有趣的是他的设计过程。他用 Arduino Uno 开始了我们许多人的工作。传感器模块，用于 VOC 和 CO₂的 CCS811 以及用于温度、湿度和压力的 BME280，都需要 3.3 伏，所以他添加了一个调节器来将 Arduino 的 5 伏电源引入范围，并添加了一些 mosfets 来进行电平匹配。不过，东西变得越来越笨重，所以他开始减少元件数量。Uno 通过剥离其已经编程的 MCU 来进行。这就消除了对稳压器和 MOSFETs 的需求，因为 3.3 伏就足够了。再经过几轮优化，最终的产品足够小巧，可以用两节 AA 电池运行。

这是从原型到产品的重要一课。它是如此的紧凑，甚至可以骑在 Roomba 的上面来测量会议室地面的空气质量。