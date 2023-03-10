# 更小的比格骨

> 原文：<https://hackaday.com/2017/04/15/an-even-smaller-beaglebone/>

众所周知，比格犬骨非常适合放在一个罐子里。即使我们现在有 BeagleBone 黑色、蓝色和绿色，这个奇怪的强大 Linux 板的形状因子仍然保持不变，并且能够放入地球上每个收银机都有的项目箱中。不过，还有另一种 Altoids 罐。Altoid mini tin 的大小刚刚超过 60×40 毫米，太小了，不适合正常大小的比格犬骨。[Michael Welling]设计了一个新的 BeagleBone 来适应这个微型项目箱。他称之为口袋骨，它就像薄荷糖一样小。

Pocketbone 基于 [Octavo Systems OSD355x 系列](http://hackaday.com/2016/05/10/new-part-day-a-beaglebone-on-a-chip/)，更广为人知的是“片上小喙骨”。该芯片采用 TI AM355x ARM Cortex A8、高达 1GB 的 DDR3 RAM、114 个 GPIOs、6 个 UARTs、2 个 SPI、2 个千兆以太网和 USB。它被封装在一个相对较大的 BGA 封装中，使路由变得容易，作为概念的证明【杰森·克里德纳】[在老鹰](https://oshpark.com/shared_projects/GWqtFu43)中建立了一个口袋骨。

[Michael]的 Pocketbone 版本基于早期的概念验证，添加了一些方便的内容。有一个 IO 扩展接头，电池输入的规定，USB 的一些固定，所有部件都在电路板的一侧，便于组装。这个版本的 Pocketbone 是使用 KiCad 创建的，这将使该项目受到开源社区的喜爱。