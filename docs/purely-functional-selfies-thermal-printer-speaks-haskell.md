# 纯功能自拍:热敏打印机说话哈斯克尔

> 原文：<https://hackaday.com/2017/12/01/purely-functional-selfies-thermal-printer-speaks-haskell/>

[Dan]最近买了一台便宜的 POS 热敏打印机，可以通过 ESP32 远程选择。完成了这个项目后，他决定看看还能让打印机做些什么。为什么不用它来打印图片？当然，已经完成了，但不是和*哈斯克尔*一起。是的，照片会有颗粒，有点奇怪，而且仅限于黑白，但是，嘿，我们喜欢这里的黑白，就像你可以做一些事情一样。

在第一个项目中，[Dan]必须想出如何与打印机对话，因为打印机附带的 RS422 电缆似乎不工作。他买了一个 TTL-RS485 适配器，但后来意识到他可以直接使用 TTL，并在其上连接了一个 ESP32/有机发光二极管开发板。在把它变成一个照相亭的过程中，他不得不切换到一个更大的屏幕和更好的刷新率。

不幸的是，[Dan]无法单独使用 Haskell。他将此归咎于 Haskell 生态系统中的蜘蛛网，对于像 Python 这样庆祝广泛使用和支持的语言来说，这不是问题。[Dan]编写了一个 Python 脚本来处理图像捕捉、显示和监听屏幕上的触摸活动，但 Haskell 最终控制打印机。休息之后请欣赏[Dan]的演示。

这个项目可能有时会尝试，但至少[丹]不需要[给它做大脑移植](https://hackaday.com/2014/09/25/thermal-printer-brain-transplant-is-two-hacks-in-one/)来让它做他想要的事情。

 [https://www.youtube.com/embed/SQreazi5PYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SQreazi5PYc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

