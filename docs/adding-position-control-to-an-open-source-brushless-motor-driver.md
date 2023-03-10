# 向开源无刷电机驱动器添加位置控制

> 原文：<https://hackaday.com/2016/02/04/adding-position-control-to-an-open-source-brushless-motor-driver/>

无刷电机现在无处不在。从遥控飞机到数控机床，如果你需要很大的动力来快速旋转，你可能会使用无刷电机。无刷电机需要一个电机控制器，对于我们大多数人来说，这意味着来自中国仓库的廉价电子速度控制器(ESC)。[本]有一个更好的主意:[建立自己的 ESC](http://vedder.se/2015/01/vesc-open-source-esc/) 。他从事这个项目已经有一段时间了，他正在完善设计，以实现一个非常酷的功能——位置控制。

[在](http://hackaday.com/2015/10/01/open-source-esc-developed-for-longboard-commute/)之前，我们已经看过了【Ben】在他的定制上的工作，家酿 ESC。从任何角度来看，它都是一件艺术品。它能够通过运行 [ChibiOS](http://www.chibios.org/dokuwiki/doku.php) 的强大 STM32F4 微控制器驱动无刷和有刷电机，该微控制器能够通过 I2C、UART 和 CAN 总线与其他微控制器通信。如果你想用电机制造任何东西——从数控机床到遥控直升机到电动长板——这就是你要的电机控制器。

[【Ben】最新更新考虑位置编码器](https://www.youtube.com/watch?v=8CcqD5sw90U)。了解电机的转速对于了解车轮的转速、电机产生的扭矩以及打造有史以来最优秀的电机控制器是非常重要的。

像上次更新一样，[Ben]演示了为这个 ESC 编写的伟大的控制程序。该 GUI 对控制器上的微控制器进行编程，提供高低压和电流保护、高转速保护、占空比改变保护，并支持再生制动。

感谢[Dudelbert]发送此邮件。

 [https://www.youtube.com/embed/8CcqD5sw90U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8CcqD5sw90U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

