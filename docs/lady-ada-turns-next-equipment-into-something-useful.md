# 艾达女士将下一件装备变成有用的东西

> 原文：<https://hackaday.com/2016/01/20/lady-ada-turns-next-equipment-into-something-useful/>

从 80 年代末到 90 年代初，[史蒂夫·乔布斯]不在苹果公司。与此同时，他建立了另一家公司 NeXT Computer，该公司将乌黑的工作站引入大学和机构，对面向对象编程进行了令人难以置信的强调，并为苹果 OS X 的 Unix-ey 风格奠定了基础。巧合的是，在 Adafruit clubhouse 有许多旧的 NeXT 设备——这并没有什么错，我们都有自己奇怪的情感和倾向。最近，[Lady Ada]将下一代电脑生态系统中最奇怪的组件之一[变成了有用的东西](https://www.youtube.com/watch?v=Aji7B9DXPHw&feature=youtu.be):电脑扬声器。

这个版本中的问题是下一个“音箱”。当不使用非常特殊的 NeXT 显示器时，NeXT 计算机通过这个奇怪的小盒子连接显示器、键盘和扬声器。NeXT sound box 有两个版本，任何一个版本的外设都互不兼容。([乔布斯]以他的设计感和对简化用户体验的渴望而闻名，你知道。)

在[Lady Ada]最初拆卸音箱时，她发现了一些关于这个外设的有趣的事情。里面有一个 I2S DAC，连接到 unobtanium DB19 连接器。理论上，I2S 装置可以用来驱动数字音频扬声器。唯一的问题是 DB19 连接器——它们很稀有，来自 Big Mess o' Wires [的[Steve]购买了世界供应](http://www.bigmessowires.com/2015/02/12/db-19-madness/)。

没有这些连接器，而且因为只有一个小时的节目，[艾达夫人]采用了最有效的黑客技术。她抓起一个 USB 音频转换器/卡，添加了一个小放大器，并将一些导线焊接到 IC 的电源和接地引脚上。它简单、有效、快速，将一个看起来很棒的 30 年前的外设变成一个有用的设备。