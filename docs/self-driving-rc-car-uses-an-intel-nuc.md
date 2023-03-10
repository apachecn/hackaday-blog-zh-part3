# 自动驾驶遥控汽车使用英特尔 NUC

> 原文：<https://hackaday.com/2016/10/10/self-driving-rc-car-uses-an-intel-nuc/>

我们不断被告知，无人驾驶汽车将成为下一个大事件。这不是什么新鲜事，随着技术的发展，我们已经看到了几十年的周期性演示。现在，我们有了在真实道路上行驶的真实原型车，而不是测试车道，尽管它们是来自财大气粗、目光长远的组织的数十亿美元的研究车辆，但这似乎开始成为我们真正有机会在消费者层面看到的一项技术。

一辆自动驾驶汽车似乎超出了普通读者的能力范围，但尽管在公共道路上制造一辆全尺寸汽车的安全防撞可能很困难，但制造一辆性能稍微适中的汽车肯定不是不可能的。[Jaimyn Mayer]和[Kendrick Tan]已经做到了这一点，[创造了一种无人驾驶的遥控汽车，它可以在没有人类干预的情况下遵循复杂的道路模式](http://jabelone.com.au/blog/make-autonomous-car-code-included/)。

[![The NUC's-eye view. The green line is a human's steering, the blue line the computed steering.](img/68bf832ec720c93348f43f10d3391546.png)](https://hackaday.com/wp-content/uploads/2016/10/demo-gif.gif)

The NUC’s-eye view. The green line is a human’s steering, the blue line the computed steering.

出乎意料的是，他们避开了许多基于 ARM 的主板作为该单元的大脑，而是采用由酷睿 i5 驱动的英特尔 NUC 迷你 PC 作为该单元的大脑。它由笔记本电脑电池组供电，并从网络摄像头接收输入。NUC 可以计算出方向和油门，并发送给处理汽车控制的 Arduino。还有一个无线电控制通道，允许汽车从自动模式切换到人工控制模式和紧急停止模式。

他们详细介绍了他们在网络摄像头上使用的偏振和中性密度过滤器，这可能会让任何对机器视觉感兴趣的人产生兴趣。他们所有的代码都是开源的，可以从他们的文章中找到链接。与此同时，休息时间下方的视频显示了他们的机器在测试线路上，以不同程度的成功完成了测试。

 [https://www.youtube.com/embed/tFwCyHdAWf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tFwCyHdAWf0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



多年来，我们已经推出了不少无人驾驶汽车，这并不是第一辆模型大小的汽车。除此之外，我们还看到了[在车库里建造的自动驾驶讴歌](http://hackaday.com/2015/12/17/self-driving-acura-built-in-a-garage/)，以及[斯坦福大学教授的自动驾驶汽车课程](http://hackaday.com/2012/02/05/build-your-own-self-driving-car/)。