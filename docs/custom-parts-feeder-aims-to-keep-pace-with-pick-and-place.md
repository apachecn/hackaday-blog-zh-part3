# 定制零件送料器旨在与拾取和放置保持同步

> 原文：<https://hackaday.com/2018/02/09/custom-parts-feeder-aims-to-keep-pace-with-pick-and-place/>

当你的小部件被证明是如此成功，以至于构建它们变得很困难时，可能是时候考虑一点机械帮助了，以拾取和放置机器(PnP)的形式。如果你打算自己动手，有很多事情要考虑，尤其是如何用零件喂养你的野兽。

管理 PnP 的胃口是[这种定制模块化零件进料器](https://blog.exploratory.engineering/post/feeder/)背后的想法，但[Hans jrgen grim stad]的在建项目中有趣的部分与设计过程有更多的关系。馈线是为了支持一个定制的并行 PnP，所以一个的需求决定了另一个的规格。主要的规格是通常的三大规格:便宜、快速、可靠。但是尺寸也是一个问题，因为 PnP 可以同时处理几十个组件卷轴。灵活性是另一个设计标准，因此可以适应不同宽度的卷轴。

考虑到这些，[汉斯]和他的公司想出了一个非常巧妙的设计。进料器的框架由印刷电路板制成，电路板上装有处理胶带的电机和控制一切的 ATmega168。胶带由激光切割链轮驱动，链轮由 3D 打印的蜗轮驱动。电路板上的指状物与制造 PnP 的铝挤压材料相匹配，并且仅比胶带宽几毫米，可以将许多馈线连接在一起。下面的视频显示了正在进行一些测试的进料器。

唉，这个构建还没有完全完成，所以如果你想为自己构建一个，你必须回头查看最终的原理图和 PCB 文件。当你等待的时候，你可能想要[建立你自己的拾取和放置](https://hackaday.com/2017/08/29/hackaday-prize-entry-a-manual-cnc-pick-and-place-machine/)。

 [https://www.youtube.com/embed/huzq4Ip_Zl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/huzq4Ip_Zl4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[托马斯兰加斯]。