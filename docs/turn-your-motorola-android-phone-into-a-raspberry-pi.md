# 把你的摩托罗拉安卓手机变成树莓派

> 原文：<https://hackaday.com/2016/08/15/turn-your-motorola-android-phone-into-a-raspberry-pi/>

摩托罗拉和法内尔/Element 14 开发了一种附加板和 SDK，可以让你将几乎任何东西连接到你的手机，这是硬件黑客成为新热点的最可靠迹象。摩托罗拉称之为“ [Moto Mods](http://developer.motorola.com/explore/system-architecture) ”系统，看起来它将成为一个专用的微控制器，与手机内部的计算机接口，并提供从 GPIOs 到 DSI(视频)的一切。自然，I2C，I2S，SPI，UART，甚至两种 USB 混合在一起。

[![dev-config-diagram-5](img/cf5b9fd5b3b53097a48e836b6d41d44c.png)](https://hackaday.com/wp-content/uploads/2016/08/dev-config-diagram-5.png)

官方 SDK，咳咳 Mods Development Kit (MDK)，基于开放的 [Greybus 协议](https://kernel-recipes.org/en/2015/talks/an-introduction-to-greybus/)栈(属于[谷歌的 Project Ara](http://www.protocolinsight.com/greybus-protocol/) 开放手机项目)，运行在 ARM Cortex-M4F 芯片上。它本身很可能是相当容易破解的，即使建议的 125 美元的价格可能是值得的，我们怀疑它只需要几美元的部件和正确的固件就可以复制。(是的，那是一个挑战。)

最初的四个适配器板从简单的试验板到树莓帽适配器(因此得名)。众所周知，手机现在可以与过去时代的超级计算机相媲美，但它们总是缺少外围接口。我们希望我们垃圾箱里的所有旧智能手机都有类似的功能。你说什么？如果你可以使用手机进行各种有用的交流，你会用手机做什么？

通过 [HackerBoards](http://hackerboards.com/modular-moto-z-android-phone-supports-diy-and-rpi-hat-add-ons/) ，感谢【Tom】的提示！