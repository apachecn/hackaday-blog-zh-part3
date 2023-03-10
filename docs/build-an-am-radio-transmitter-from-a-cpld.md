# 用 CPLD 制作调幅无线电发射机

> 原文：<https://hackaday.com/2015/11/12/build-an-am-radio-transmitter-from-a-cpld/>

[Alex Lao]一直在摆弄 PSoC 的 CPLD 类部件。也就是说，他一直在用软件“在硬件中”实现简单的逻辑功能。在[通过习惯不同的时钟源](http://www.voltagedivide.com/2015/09/21/cypress-psoc-5lp-intro-and-clock-configuration/)开始使用芯片后，他[建造了一个以 24 MHz 传输的简单 AM 无线电。](http://www.voltagedivide.com/2015/10/16/psoc-am-radio-transmitter/)

[亚历克斯]正在学习的设备是一个 [Cypress PSoC 5LP](http://www.cypress.com/products/psoc-5lp) ，或者更具体地说是[他们的(廉价)零件原型套件](http://www.cypress.com/documentation/development-kitsboards/cy8ckit-059-psoc-5lp-prototyping-kit)。该芯片本身是一个 ARM 微处理器内核，带有 CPLD 和一些模拟小程序，使微处理器与外界的接口更加容易。[Alex]他甚至不摆弄微处理器，他对学习 CPLD 方面的东西很感兴趣。

[![PRS-Circuit](img/881850608ad7122bee4eff9edb520cf6.png)](https://hackaday.com/wp-content/uploads/2015/11/prs-circuit.png) 他从一个 24 MHz 的载波和一个 1 kHz 的音调信号开始，用一个逻辑与函数把它们组合起来。提示音开启时，载波播放通过；这是调幅广播最基本的内容。一切都是逻辑(方波)，所以这是一个混乱的无线电信号，但它会完成任务。

预先添加一个多路复用器可以让[Alex]在他的“广播”电台上播放两种音调。对于一些简单的逻辑来说还不错，对于 CPLD 来说是一个奇妙的 Hello World 项目。我们迫不及待地想知道[亚历克斯]下一步要做什么！

如果你对一般的 CPLD 或 Cypress 这样的 CPLD +微系统感兴趣，那么[Alex]正在使用的开发套件看起来是一种廉价而轻松的开始方式。(相对而言，PSoCs 比更简单的 8 位微处理器或 Arduino 要高出一两步。)Hackaday 自己的[Bil Herd]有一个关于如何开始使用 Cypres PSoC 系列的另一个成员的视频，所以你也应该看看。