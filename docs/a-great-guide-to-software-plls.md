# 软件 PLL 的伟大指南

> 原文：<https://hackaday.com/2017/09/10/a-great-guide-to-software-plls/>

有些事情你认为你很了解，因为你年轻时学过，你了解它们的运作原理。然后在你的晨间饲料中出现了一个链接，提醒你你知识的极限，你意识到有一个全新的理解水平要达到。

以锁相环(PLL)为例。您了解它们的工作原理，使用它们进行频率合成，并且知道它们还可以做其他事情，例如恢复有噪声的时钟线路和进行 FM 解调。但是当你阅读【保罗·卢图斯】 *[了解锁相环](https://arachnoid.com/phase_locked_loop/index.html)* 一页时，一个全新的前景就展现在你面前。

作为天气传真解码器项目的一部分，他在软件背景下讨论 PLL，这为我们这些通过硬件(如古老的 4046 CMOS 芯片)了解 PLL 的人提供了一个视角。我们可以很容易地看到不同参数的不同 PLL，例如，它们与窄带环路滤波器一起使用，以检索淹没在噪声中的信号，所有这些都是通过一些简单的代码调整，而不是大量的电路。这是一个已经有几年历史的页面，但是像这样的资源不会老化。

如果 PLL 对你来说是全新的，那么你需要重温一下去年 Hackaday 自己的【Al Williams】的[优秀 PLL 入门](https://hackaday.com/2016/03/23/unlock-the-phase-locked-loop/)。

【via [黑客新闻】](https://news.ycombinator.com/item?id=15189325)

[PLL 图:Chetvorno [CC0](https://commons.wikimedia.org/wiki/File:Phase_locked_loop.svg)