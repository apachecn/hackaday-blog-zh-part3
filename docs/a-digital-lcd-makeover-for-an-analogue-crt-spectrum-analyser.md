# 模拟 CRT 频谱分析仪的数字 LCD 改造

> 原文：<https://hackaday.com/2017/08/20/a-digital-lcd-makeover-for-an-analogue-crt-spectrum-analyser/>

[Seb Holzapfel，VK2SEB]有一个相当不错的频谱分析仪，惠普 141T。这是一个完全模拟的仪器，所以它缺少一些你可能会在它的现代对应物上看到的复杂功能。

HP 具有的一个特性是垂直偏转输出，它实际上允许在示波器上再现轨迹。[Seb]利用这一点，将其应用于 STM32F746 Discovery board 及其相关的 LCD 触摸屏，以[为惠普生产一个包括现代功能](http://sebholzapfel.com/lcd-upgrade-for-the-hp-141t-spectrum-analyzer-part-1/)的界面，如轨迹标准化和瀑布视图。在这一过程中，他必须制作一个电压电平转换器，将惠普的扫描输出转换到 ST 电路板可接受的范围内。

他详细介绍了他为这个项目开发的软件，他煞费苦心地提醒我们，这个项目仍然是一项正在进行的工作。他指出，惠普有一系列其他输出(在那些包括同轴连接器的“D”插座上)，提供有关其波段和扫描设置的信息，因此有足够的可能性进一步定制。

如果你对这个项目感兴趣，那么[代码可以通过 GitHub](https://github.com/schnommus/stm32_hp141_lcd) 获得，否则你可以在休息时观看他的视频。他把它标为“第一部分”，所以我们期待这个项目的更多内容。

 [https://www.youtube.com/embed/CwwRvqHGyts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CwwRvqHGyts?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果[Seb]听起来很熟悉，那可能是因为我们最近介绍了[他的微波带状线滤波器原型](http://hackaday.com/2017/07/25/rapidly-prototyping-rf-filters/)。