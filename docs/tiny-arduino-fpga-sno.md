# 微型 Arduino + FPGA = Sno

> 原文：<https://hackaday.com/2018/04/30/tiny-arduino-fpga-sno/>

去年年底，Alorium 推出了一款新产品，引起了我们的注意。Sno (发音像“snow”)板是一个很小的 Arduino 板，你可以在下面的视频中看到。这本身并不有趣，但 Sno 也有一个 Altera/Intel Max 10 FPGA 板载。如果您不是 FPGA 用户，请不要放弃，因为虽然您可以通过多种方式定制 FPGA，但您不必这样做。

像 Alorium 的 XLR8 产品一样，FPGA 带有预编程的功能和匹配的 Arduino API 来使用它们。具体来说，有模块做模数转换，伺服控制，操作新像素，并做浮点数学。

不过，如果您愿意，可以对 FPGA 进行重新编程，使其具有其他功能，即 XBs 或 Xcelerator 模块。我们看到的唯一问题是，到目前为止，它们并不多。除了股票 XBs，有一个将做正交解码处理轴编码器之类的东西。你可以在他们的 [GitHub](https://github.com/AloriumTechnology) 页面上找到一些其他的。你可以通过[查看 XLR8 电路板的教程](http://www.aloriumtech.com/xlr8-quickstart/)来了解工作流程。

当然，你可以按照自己的想法编写自己的 FPGA 配置，但它们也提供了一个标准的工作流程——open XLR 8——让你可以构建自己的模块，就像它们的模块一样工作。很容易想象一个“应用程序商店”的概念，人们开发定制的程序块并提供给用户。

我们真的很喜欢这个设备的想法，它肯定是便宜的。你可以在 XLR8 上做原型，它看起来像一个 UNO，或者你可以在 Sno 中放置标题。他们还出售一个分线板，这将使 Sno 在物理上更像一个 UNO。然而，我们感到惊讶的是，在过去的两年中，没有创建更多的 XB。

板载 FPGA 类似于我们今年早些时候看到的箭头板上的 FPGA，尽管它有一些额外的组件，如 SDRAM。如果你正在寻找一个项目，把我们的 PWM 代码转换成 XB[可能会很有趣。](https://hackaday.com/2015/12/17/pwm-on-the-lattice-icestick/)

 [https://www.youtube.com/embed/h1AwhgA1BDI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/h1AwhgA1BDI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢【K5STV】给我们展示了其中的一个。