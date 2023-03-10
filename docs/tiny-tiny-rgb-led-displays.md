# 微小的 RGB LED 显示屏

> 原文：<https://hackaday.com/2016/06/12/tiny-tiny-rgb-led-displays/>

Hackaday.io 贡献者 extraordinaire [al1]最近一直在摆弄小 led，这不可避免地导致摆弄大组小 led。准确地说，是微小的 RGB 发光二极管矩阵。

[![Where's the LED?](img/960a470e0fcfcb24d3ef9465cf362696.png)](https://hackaday.com/wp-content/uploads/2016/06/8016421457708151315.jpg)

Where’s the LED?

首先，他将 128 个 0404 SMD RGB LEDs(是的，每边 40 千分之一英寸)塞进一个不到 37 毫米 x 24 毫米的电路板上。他将该项目称为 [384:LED](https://hackaday.io/project/8789-384led) (毕竟，这 128 个封装中的每个封装内部都有三个二极管)。微控制器和驱动芯片位于单独的驱动板上，该驱动板通过引脚接头搭载到 LED 板上。当然，他不得不使用 0.05 英寸的接头，因为这东西真的很小。

当然，没有一个项目是没有缺陷的。[al1]错误地购买了尺寸错误的 led，所以他剩下了一堆(略有不同的)0404 LEDs。是时候做一个 8×8 矩阵了！然而，LED 并不仅仅是第一个被砍掉一半的项目。这是一个完整的重新设计，四层板和背面的微控制器。作为一个需要大量极端焊接的 scrounge 项目，他甚至从一台[廉价数字调频收音机](http://hackaday.com/2014/11/12/2-fm-transmitter-for-rasberry-pi/)上取下了微控制器。太棒了。

我们对[al1]微小的黑客技术感到敬畏。现在是时候在这些小显示器上显示一些同样酷的图形了。