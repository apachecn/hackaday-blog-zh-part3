# LED 矩阵故障及维修

> 原文：<https://hackaday.com/2015/09/07/led-matrix-failure-and-vindication/>

如果需要是发明之母，那么失败是什么之母？改善？不管怎么说，[【PRP 鼠疫】的第二版他的可卷式 70×30 RGB LED 显示屏](http://www.elinux.org/LED_Matrix_Failure)看起来比第一版好很多，也更可靠，而这恰恰是因为“失败”。

有时你围绕软件设计硬件，有时反之亦然。这都是关于痛苦的平衡。[PRP pages]最初以一致的从左到右[光栅](https://en.wikipedia.org/wiki/Raster_scan)排列将条带连接在一起，以使编码更容易，但这意味着织物背面的长导线从右侧回到左侧的起点。这些长电线挂在东西上，把焊接点扯开了。

[![600px-Dotstar-adapter-solder3](img/4703bfaff8d6d9f7551c01d2c033e44d.png)](https://hackaday.com/wp-content/uploads/2015/09/600px-dotstar-adapter-solder31.jpg) 修罗？从左到右与从右到左交替排列，以最大限度地减少布线，并为端子提供美观、坚固的连接器，以更复杂的软件驱动器件为代价，实现更加优雅的方案。(交替行必须水平翻转，因此这意味着自定义驱动程序例程。)

第二个问题是[PRP peace]使用的接口板在 SPI 线路上没有足够的电流源能力，他发现如果第一个像素距离板超过 24 英寸，他就不能与串可靠地通信。然而，一旦信号到达第一个像素，一切都好了。[PRP peace]发现 RGB LEDs 本身比 SPI 源具有更强的驱动能力。

解决办法？在链的前端添加一个像素来缓冲 SPI 线，并用作奖金状态指示器。可爱。

我们很难称之为“失败”，而是“学习经历”。无论如何，这里有两个设计“错误”是我们在制作可卷曲柔性像素显示器时不会犯的。谢谢。