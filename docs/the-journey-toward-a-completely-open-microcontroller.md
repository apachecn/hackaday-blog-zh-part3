# 完全开放的微控制器

> 原文：<https://hackaday.com/2016/10/10/the-journey-toward-a-completely-open-microcontroller/>

![mriscv](img/f6af991fdcb99d6bff7e0cf7ad958509.png)

An annotated mRISCV die image

我们不知道你们怎么想，但是使用完全开放硅的 Arduino 级微处理器板的想法对我们来说是一个非常有吸引力的前景。这正是[【onchipUIS】的](https://twitter.com/onchipUIS)既定目标。他们是桑坦德工业大学[研究小组](http://www.uis.edu.co/)的一部分，设计并录制了一个具有类似 M0 皮层特征的 [RISCV](https://riscv.org/) 实现。

RISCV 项目为现代 32 位 CPU 开发了一个开放的 ISA(指令集架构)。超过 40 个研究小组和公司已经加入到这个项目中，并且正在一起实施。

[onchipUIS]就是这样一个项目。他们的推特时间表显示了他们最近取得的快速进步。

![mriscv_bonding](img/df08d653620b4fbd36bf0be0ff71de55.png)

Die directly bonded to an OSHPark PCB

流片后，他们开始试验新的引线键合机。在新型平台上进行引线键合，尤其是手工键合，是一个充满问题的过程。[onchipUIS]不仅成功地焊接了他们的芯片，而且他们还使用了一种板上芯片工艺，将芯片直接焊接到 PCB 上。他们使用了 OSHPark 的公告板，并在 Twitter 上描述了 T2 的流程。

他们构建的电路板拆分了所有芯片外设，是一个方便的测试设置，可以帮助他们验证平台。检查它，和一些高分辨率的模具图像，在下面。他们也给我们发来了一个芯片图像，用的是[我们在](http://41j.com/blog/2016/09/random-sem-images-mcm68364-64kb-rom/) [hackerfarm](http://www.hackerfarm.jp/) 的电子显微镜，我们期待结果！

![mrisc_board](img/2a7c84c998fa7121921cabbadca1ed17.png)

The current mRISCV board

> [@ico_TC](https://twitter.com/ico_TC) 较慢的 gif。足以看到 RAM 和触发器的总线连接。[# tech](https://twitter.com/hashtag/tech?src=hash)[@ SSCSociety](https://twitter.com/SSCSociety)[@ IEEE cassociety](https://twitter.com/ieeecassociety)[# happy October](https://twitter.com/hashtag/HappyOctober?src=hash)[# maanavotosí](https://twitter.com/hashtag/Ma%C3%B1anaVotoS%C3%AD?src=hash)[pic.twitter.com/9EopcditiQ](https://t.co/9EopcditiQ)
> 
> —onchip(@ onchipUIS)[2016 年 10 月 1 日](https://twitter.com/onchipUIS/status/782334495974391808)