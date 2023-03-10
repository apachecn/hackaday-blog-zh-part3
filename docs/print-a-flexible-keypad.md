# 打印柔性键盘

> 原文：<https://hackaday.com/2017/08/15/print-a-flexible-keypad/>

[Micah Elizabeth Scott]需要一个包裹在柱子周围的定制 USB 键盘。她找不到她想要的东西，所以她用柔韧的 Nijaflex 细丝设计并打印了它。你可以在下面的视频中看到设计过程和结果。

电子设备依赖于一个 Teensy，它可以很容易地模仿 USB 键盘。按键本身使用旧的电阻分压器技巧，允许 Teensy 上的一个模拟输入读取多个按钮。这很方便，但也最大限度地减少了柔性 PCB 上的布线。

电路板本身使用的是研磨而不是蚀刻的 Pyralux。除了在更传统的 CAD 程序中完成的轮廓之外，大部分 PCB 插图都是在 KiCAD 中完成的。

我们总是喜欢看到黑客级 3D 打印机的实际应用。毕竟你能做的钥匙扣就那么多。当然，你可能并不完全需要这种键盘布局。但是，制造柔性 PCB、印刷键盘本身以及将一切与电子设备集成在一起的技术将是任何类似项目的伟大路线图。

据我们所知，这只猫对最终的设计没有任何实际贡献。或许，除非你把鼓舞人心的灵活性也算在内。

我们已经看到有人使用 [Pyralux 和 Ninjaflex 作为抗蚀剂](http://hackaday.com/2014/10/28/make-flexible-pcbs-with-your-3d-printer/)来制作实际的 PCB，如果你不想研磨电路板的话。这也不是我们第一次看到一个小小的[被压进键盘控制器服务](http://hackaday.com/2017/02/13/vintage-laptop-keyboard-types-again-through-usb/)。

 [https://www.youtube.com/embed/zultG4QwgTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zultG4QwgTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢[凯尔]的提示。