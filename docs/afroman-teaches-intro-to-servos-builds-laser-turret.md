# 一个女人教伺服系统入门，建造激光炮塔

> 原文：<https://hackaday.com/2018/01/07/afroman-teaches-intro-to-servos-builds-laser-turret/>

在长时间的中断之后，我们很高兴地看到了来自[一个女人]的新视频，她是互联网提供的最容易接近和最会说话的老师之一。如果你是电子产品的新手，看看前面的句子，并决定看看他的精彩视频。新的一个是所有关于伺服系统，它在一个简单的构建中达到高潮，为探索机器人技术提供了基础。

[【阿弗曼】在他的巡回赛](https://www.youtube.com/watch?v=iH9_xtulyws)中没有留下任何未完成的任务，这是在休息后嵌入的。他解释了开环与闭环电机系统之间的差异，讨论了不同大小和类型的伺服系统，并走过了在项目中使用它们的号角和尾纤。最后，他将这一知识应用于基于云台平台建造的激光炮塔。

Arduino 驱动的炮塔使用两个由 pots 控制的微型伺服系统，在 X/Y 空间按度数移动。有趣的是，[Afroman]并没有使用连线对 Arduino IDE 中的电路板进行编程。相反，他使用一种叫做 [XOD](https://xod.io) 的开源微控制器语言/IDE，让你通过拖放组件和逻辑节点构建一种智能的原理图来进行编码。绘制连接，分配您的 I/O 引脚编号，XOD 将编译代码并直接上传到电路板。

对于初学者来说，XOD 似乎是一个很好的快速原型制作工具。另一方面，查看生成的代码会发现大量的包装器，这些包装器混淆了实际执行任务的代码。似乎也没有办法摆脱它们，所以一旦你用 XOD 设计了某个东西，你就会陷入用它来迭代的困境。也就是说，生成的代码有很好的文档记录，知道自己在看什么的人可以找到，例如，分配给闪烁草图 LED 的 I/O 引脚。

一旦双激光猫折磨者的新鲜感消退，使用你购买的 5 包中的其他伺服系统来[按动灯开关](https://hackaday.com/2017/01/17/servo-controlled-iot-light-switches/)，[控制旋钮](https://hackaday.com/2016/12/26/modified-servo-adds-focus-control-to-telescope/)，或者[演奏钟琴](https://hackaday.com/2017/11/23/swarm-of-servos-plays-this-robotic-glockenspiel/)。

 [https://www.youtube.com/embed/iH9_xtulyws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iH9_xtulyws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

