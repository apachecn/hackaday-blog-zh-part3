# 完全拥有你从未拥有过的 Dreamcast 插件

> 原文：<https://hackaday.com/2017/07/17/completely-owning-the-dreamcast-add-on-you-never-hadcompletely-owning-the-dreamcast-add-on-you-never-had/>

如果你有一台 SEGA Dreamcast 在某个地方的壁橱里踢来踢去，并且你仍然有一个未被充分利用的附加视觉记忆单元(VMU)，你今天就可以享受一下了。如果没有，但你喜欢对稍微老化的硅片进行难以置信的详细研究，你会更加兴奋。因为[德米特里·格林伯格]有一个 VMU 黑客，它的完整性会让你敬畏。随着所有的位到位，黑客计数是一个新的 MAME 仿真器，一个 IDA 插件，一个前所未有的 ROM 转储，以及一个不存在的 ARM 芯片的仿真器，运行 Flappy Bird。全部在一个月的工作中！

VMU 是 Dreamcast 的附加产品，主要将游戏数据存储在闪存中，但它也有一个小型 LCD 显示器，一个 D-pad 和 VMU 内部通信功能。它也有独立游戏的空间，可以以有限的方式与主要的 Dreamcast 游戏互动。[德米特里]想看看他还能用它做些什么。基本上什么都有。

我们无法在一篇简短的文章中公正地解释这一点，但概要是，他从 VMU CPU 的数据表开始，并寻找有趣的说明。然后，他开始对 SDK 附带的 ROM 进行逆向工程，这只是微不足道的混淆。一路走来，他为芯片编写了自己的 IDA 插件。两个 [ROP 小工具](https://en.wikipedia.org/wiki/Return-oriented_programming)的发现让他可以将 ROM 转储到闪存中，在那里可以很容易地读取。VMU 社区的人会喜欢第一个 ROM 转储。

开始用这个设备做一些有用的事情！[Dmitry]对“有用”的定义是让它模拟现代 CPU，以便更容易编程。当然，没有人直接在过时的硬件上为现代硬件编写仿真器——您首先要在笔记本电脑上仿真过时的硬件，以获得调试环境。所以[Dmitry]将他在 MAME 找到的 VMU CPU 的仿真器从 C++移植到 C(原因我们都明白)，并为 VMU 的硬件进行了定制。

在仿真的 VMU 中，[Dmitry]编写了 ARM Cortex 仿真器，它将很快运行。但是模仿什么样的大脑皮层呢？Cortex-M0 可能已经足够好了，但它缺少一些[Dmitry]喜欢的指令，所以他最终编写了一个无硅 Cortex-M23 的仿真器，它具有他想要的功能。在 VMU 中加载 Cortex 模拟器，你可以用 c 语言为它编写游戏。[Dmitry]自然地提供了两个演示:Mandlebrot set grapher 和 Flappy Bird。

惊叹？是啊，我们也是。但这是同一个人在 AVR 架构上模拟 ARM 芯片，只是为了在 ATMega1284p 上运行 [Linux。](http://hackaday.com/2012/03/28/building-the-worst-linux-pc-ever/)

 [https://www.youtube.com/embed/muSEUOaiJqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/muSEUOaiJqE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

