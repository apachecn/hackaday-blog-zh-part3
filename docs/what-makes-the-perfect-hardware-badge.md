# 是什么造就了完美的硬件徽章

> 原文：<https://hackaday.com/2017/01/10/what-makes-the-perfect-hardware-badge/>

只有少数几个人可以说他们已经为会议设计了几个成功的电子徽章。沃佳·安东尼奇不仅仅在这个名单上，他是这个领域的领导者之一。在这种类型的设计挑战中有很多压力:美学、功能性，当然还有可制造性。如果你想知道如何制作一款会受到用户喜爱的裸露 PCB 产品，你需要研究一下 Voja 在 2016 Hackaday SuperConference 徽章上的工作。徽章是完全开放的，所有的设计文件、固件和手册都在[徽章项目页面](https://hackaday.io/project/16401)上。

从贝尔格莱德到帕萨迪纳，在会议截止日期前指导 300 枚徽章在终点线的制作，Voja 生病了。他参加了会议，但没有声音，他让我为他做徽章设计演讲。你可以看看下面的谈话，但让我们简单地谈谈为什么 Voja 的设计如此壮观。

### 美学

会议徽章的目的是让与会者把它们戴在脖子上。这使得美学和设计的其他方面一样重要。每个人都将以这种方式与徽章互动。

Voja 的方法是想出一系列电路板轮廓和主要元件布局(在线框图中)。然后，他向许多不同的人寻求意见，帮助将六个设计缩减为一个想法。选定设计后，Voja 调整了配色方案，运行了一批原型，并开始组装电路板。

他最后的改进使得徽章如此美丽。他从黑色光滑阻焊膜转向黑色哑光，将丝网颜色与辅助按钮的颜色和非照明 led 的色调相匹配。外形、组件放置(led 和按钮呈 45 度角)以及边缘安装电池座的选择(采用 PCB 切口，体积更小)都是标志性的设计元素。

### 五金器具

设计对价格有一定影响(可以制造吗？)但硬件选择是这其中最大的驱动力。徽章上有三个 IC，PIC18F25KL50，一个 LED 驱动器和加速度计。其余的相当简单，一个红外接收器，迷你 B USB 插孔，发光二极管，按钮和无源器件。关键是这里没有真正的异国情调。用得好的话，普通部件可以很容易地创造出人们喜欢的设备。坚持在 BOM 成本内完全是另一个问题。我们让它接近我们的目标，但那是因为我们团队的许多劳动力没有计算到底线。阅读更多关于[我们制造](http://hackaday.com/2016/11/25/a-tale-of-electronic-manufacturing/)的故事。

### 功能

如果电子会议徽章只挂在与会者的脖子上，那它就是失败的。人们需要与这些徽章互动，为此 Voja 增加了一个俄罗斯方块游戏，滚动信息可以通过 con 上的红外信息亭定制，以及使用加速度计的重力模拟

基础是我们的微芯片朋友提供的 USB 引导程序。这为徽章增加了 USB 大容量存储支持。Voja 写了一个“内核”,运行在受保护的引导装载空间，负责所有的底层硬件处理。这种组合使徽章适合所有技能水平。

一切都是[内存映射](https://github.com/Hack-a-Day/2016-Hackaday-SuperConference-Badge-Hacking/blob/master/HaD_Badge.h#L122)—led 控制缓冲器、去抖按钮读数、IR 总线上的 RX 和 TX、加速度计数据子程序调用、时序和随机数。而 Voja 的巧妙实现是先把中断扔给用户空间。大多数用户会将其重定向回引导加载程序，但经验丰富的嵌入式程序员可以通过不将控制权交还给内核来获得对硬件的完全访问权。

这些特性对于固件来说是一个巨大的胜利。但是 Voja 写了第二个固件。直到骗局已经开始，他才透露出来。用户可以将这种选择闪现到徽章上，接受[加密挑战](http://hackaday.com/2016/11/16/solving-hackadays-crypto-challenge/)。

 [https://www.youtube.com/embed/q3ojx8zSe9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q3ojx8zSe9Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Voja Antonic 是一个了不起的硬件创造者。翻看他的作品目录，你会对他的[达利钟](https://hackaday.io/project/5705-in-memory-of-dali)和 [FR4 围栏](http://hackaday.com/2015/06/03/how-to-build-beautiful-enclosures-from-fr4-aka-pcbs/)感到惊讶。他为所有人树立了榜样——你应该成为一名伟大的硬件工程师、伟大的设计师，并在你的设计中加入令人惊叹的文档。这个会议徽章达到了所有这些标准，甚至更多。