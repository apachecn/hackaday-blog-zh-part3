# 使用 Involt 实现快速简单的物联网原型制作

> 原文：<https://hackaday.com/2017/02/04/quick-and-easy-iot-prototyping-with-involt/>

物联网、网络应用和联网设备都变得越来越受欢迎。但是，市场仍然像一个狂野的西部药剂师，没有一个单一的物联网生态系统或架构似乎是我们最终都会使用的一瓶蛇油。因此，我们黑客热衷于制造自己的设备，而不是冒着被锁定在随时可能过时的物联网系统中的风险。但是，构建物联网设备和界面需要广泛的技能，那些缺乏黑暗编程艺术技能的人可能很难为他们闪亮的新联网设备创建控制应用程序。

[进入 Involt](https://hackaday.io/project/11615-involt-prototyping-framework) ，这是一个使用 HTML 和 CSS 构建硬件控制界面的框架。该框架是建立在 Node-Webkit 之上的，这意味着那些有一点 web 开发背景的人应该熟悉这些约定。硬件交互(在 Arduinos 上)用简单的 CSS 类来处理。例如，一个按钮可能包含一个 CSS 类，它将 Arduino 引脚从高电平变为低电平。

Involt 可以获取 CSS 并将其转换为函数，然后通过串行或蓝牙通信将其发送到 Arduino。对于更高级的功能，可以使用 Javascript(或者任何其他语言)来定义生成什么功能，然后发送到 Arduino。但是，许多物联网设备所需的基本功能(可能只需要打开和关闭，或者设置为某个值)只需要一点 HTML 和 CSS 知识。您将在一个具有 CSS 样式和功能的 HTML 布局中创建界面和底层硬件交互。

虽然 Involt 不是唯一简化硬件交互的框架(它甚至不是唯一基于 [Node.js 的方法](http://hackaday.com/2016/12/22/solving-iot-problems-with-node-js-for-hardware/))，但这种简单性绝对值得称赞。对于那些刚刚开始使用这类设备的人来说， [Involt 绝对可以让这个过程变得更快，痛苦更少](http://involt.github.io)。而且，即使对于那些*在这个领域很有经验的人来说，用 Involt 制作原型的速度和效率肯定是有用的。*