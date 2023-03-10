# 简单的太阳能泥瓦罐灯

> 原文：<https://hackaday.com/2016/01/07/simple-solar-mason-jar-lights/>

[迈克尔·莫根森]制作了[萤火虫罐](https://hackaday.io/project/8978-firefly-jar)——一个简单的电路点亮标准梅森罐内的![firefly_jar_01](img/2819b23297125988e327725f895c168c.png)闪烁的 led，在假期送给朋友和家人。鉴于它的简单性和通孔设计，它是一个“学习焊接”类或那些想开始构建一些真正简单的电子产品的理想项目。只有几个零件，组装起来不会花很长时间。鉴于他已经提供了所有的[源设计文件](https://github.com/mogenson/firefly-jar)，其他人剥离这个项目应该很容易。

一个 55 毫米的太阳能电池安装在 63.5 毫米直径的 PCB 上，而 PCB 又可以完美地安装在一个带圆盖的标准梅森罐中。在阳光下，太阳能电池为两节 1.2V 镍氢电池充电。这也会关闭 P 沟道 MOSFET，从而关闭 LED。只有当太阳能电池电压较低且镍氢电池充电时，LED 才会亮起。2.1V LDO 直接驱动内置闪烁电路的两个 led，无需任何其他部件。看看下面萤火虫罐子的视频。

 [https://www.youtube.com/embed/_lKYfi4vv54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_lKYfi4vv54?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

