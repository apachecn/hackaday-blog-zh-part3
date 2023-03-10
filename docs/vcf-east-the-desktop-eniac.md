# VCF 东部:桌面 ENIAC

> 原文：<https://hackaday.com/2018/05/24/vcf-east-the-desktop-eniac/>

ENIAC，或电子数字积分器和计算机，本质上是你现在阅读这些文字的设备的曾祖父。它是在第二次世界大战期间开发的，价值约为今天的 700 万美元，用于计算火炮射表。一旦关于其能力的消息传出，它也被投入到诸如协助约翰·冯·诺依曼研究氢弹等令人兴奋的任务中。ENIAC 的成功直接导致了 EDVAC 的发展，它采用了一些现在标准的计算概念，如二进制算术和存储程序的思想。其余的，正如他们所说，都是历史了。

[![](img/8b137920d2740f0a76889cc5280f9732.png)](https://hackaday.com/wp-content/uploads/2017/01/programming-the-eniac-computer-thumb.png) 但是 ENIAC 不仅仅是昂贵和成功，它也是普通的*巨大的*。虽然这对现代人来说有点难以理解，但 ENIAC 大约有 100 英尺长，重达 27 吨。在 1956 年的最终配置中，它包含了大约 18，000 个真空管、7，000 个二极管、70，000 个电阻器、10，000 个电容器和 6，000 个开关。所有这些硬件都有强大的电力需求:ENIAC 可以轻松吸收 150 千瓦的电力。当时，对于一台每秒可以执行 5000 条指令的机器来说，这一切似乎完全合理，但今天 Arduino 可以绕着它转圈。

现代硬件与这种原始计算机之间在能力和尺寸上的巨大差异在东方复古计算机节上得到了充分展示，Brian Stuart 展示了他令人印象深刻的 ENIAC 仿真器。像任何优秀的老式硬件模拟器一样，他的项目不仅准确地再现了原始硬件的功能，而且试图让现代操作员体验操作机器的独特体验，这种体验在“计算机”仍然是使用计算尺的人的全盛时期曾有过。

## 你能走多低？

鉴于 ENIAC 的计算能力与 Raspberry Pi 之类的平庸之作之间的巨大差距，人们很自然会想知道要模拟硬件需要多少抽象。在处理较旧的硬件时，我们偶尔会谈到“周期精确”仿真:这实质上意味着仿真器可以从原始机器上运行软件，而无需修改软件。就运行在模拟器上的软件所关心的内容而言，模拟器是准确的，但这并不意味着底层方法是相同的。这使得仿真器可以运行旧软件，同时使用现代技巧来帮助提高整体性能。

但是对于像 ENIAC 这么慢的计算机，速度真的不是问题。我们有足够的能量可以燃烧，所以你能有多精确？最初，Brian 认为在电路层面上模拟 ENIAC 会很有趣。但是考虑到器件数量，以及文档中实际上只有对内部电路的粗略解释，他认为这可能是一个很高的要求。最后，他决定将 ENIAC 模拟到机器运行时通过机器的实际脉冲。这种程度的仿真使他的软件异常准确，而且它确实可以运行原始 ENIAC 技术手册中的任何示例程序，但这确实意味着即使在现代计算机上，仿真运行速度也比实际的 ENIAC 慢。但是保真度的提高，特别是对于那些希望真正了解早期计算机如何工作的人来说，值得等待。

## ENIAC 体验

为 ENIAC 创建一个命令行模拟器会更容易，只需将结果转储到终端即可(事实上其他人已经这样做了)，但这不会给你实际运行一台大到足以占据一栋大楼的计算机的感觉。为此，Brian 使用 ENIAC 面板的实际图像创建了许多视觉效果。这给用户的印象是，实际上站在计算机前，看着银行愉快地眨眼，因为它通过给定的程序工作。

 [![eniac_inside2](img/b6bcd4a93df89b0f8609d02afdeb0308.png "eniac_inside2")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/05/eniac_inside2.jpg?ssl=1)  [![eniac_inside](img/855144600425e4aca281c494d61093d7.png "eniac_inside")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/05/eniac_inside.jpg?ssl=1) 

虽然不要求使用仿真器，但 Brian 甚至重新创建了 ENIAC 操作员会使用的手持控制单元。他提到这个外围设备经常被忽视，在他的研究中，他只能找到一张设备的清晰照片，作为他 3D 打印模型的基础。

 [![eniac_controller](img/5b456713be02dc3f9e9c5b48ae4807b5.png "eniac_controller")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/05/eniac_controller.jpg?ssl=1)  [![eniac_inuse](img/7abe69d7dc0218d4c4c93898a5341497.png "eniac_inuse")](https://i0.wp.com/hackaday.com/wp-content/uploads/2018/05/eniac_inuse.jpg?ssl=1) 

## ENIAC:主场比赛

Brian 已经为他的 ENIAC 模拟器提供了源代码和编译的二进制文件，任何人都可以尝试控制原始“大铁”的虚拟表示。他甚至为低至 C.H.I.P ( [如果你能找到一个，那就是](https://hackaday.com/2018/04/03/is-this-the-end-for-the-c-h-i-p/))的机器提供了二进制文件，所以不需要太多设备就能让你自己的 mini ENIAC 启动并运行。不过，你必须提供[自己的氢弹来研究](https://hackaday.com/2015/09/11/fermiac-the-computer-that-advanced-the-manhattan-project/)。

如果你想上一堂关于野兽编程的外星方法的速成课，我们自己的 [Al Williams 最近写了一篇关于 ENIAC](https://hackaday.com/2017/01/31/eniac-the-way-we-were/) 的精彩文章，包括一些在虚拟环境中操作它的信息。