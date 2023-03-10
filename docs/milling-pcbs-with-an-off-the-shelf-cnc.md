# 用现成的 CNC 铣削 PCB

> 原文：<https://hackaday.com/2016/02/28/milling-pcbs-with-an-off-the-shelf-cnc/>

在你从一个过程中获得[伟大的结果之前，有很多小事情可能会出错。我们喜欢阅读构建日志，从所犯的错误中学习。[Marc Li yange]从 Carbide3d 购买了一台 Nomad CNC 机器，经过一点学习，已经从中获得了一些非常好的 PCB。](http://community.carbide3d.com/t/great-results-milling-pcbs-from-eagle-with-the-nomad/283)

他遇到的第一个问题是没有在 EagleCAD 中设置设计规则来检查对于他的路由器位来说太小的间隙。在他解决了这个问题之后，Carbide 不支持曲线的 R 值；而不是选择 IJK，他做了一个很好的 TQFP 浸打破董事会。

下一块板是更复杂的双面工作。他巧妙地让机器在 PCB 上钻了两个孔，为两个定位销留出了空间。不幸的是，这并没有完全按照计划进行，他与一些过孔有轻微的错位。看起来没问题，他开始组装。令他沮丧的是，许可又被取消了。这对我们来说有点似曾相识的感觉。

我们已经在数控机床上制作了很多电路板，可以证明这项任务的挑剔性。对于有很多小孔的电路板，这肯定比光致抗蚀剂技术要快。一个人要尝试很多次，才会开始成功多于失败，但这是非常值得的。