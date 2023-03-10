# AT 至 XT 键盘适配器

> 原文：<https://hackaday.com/2017/01/21/attoxtkeyboard/>

如果你有一台旧的 PC/XT 存放在地下室的某个地方，想用一个新的键盘，这里有一个你可能会喜欢的小项目。[Matt]使用 AT 转 PS/2 键盘电缆在原型板上构建了一个 [AT2XT 键盘适配器](http://tech.mattmillman.com/building-an-at2xtkb-at-to-xt-keyboard-adapter-on-prototype-board/)。AT2XT 键盘适配器基本上允许用户将 AT 键盘连接到 XT 类计算机，因为 XT 端口在电子方面与 PC/AT 键盘类型不兼容。对于那些拥有大量旧电脑的复古计算爱好者来说，将 XT 机器连接到 KVM(键盘/视频/鼠标)开关将是一个很好的技巧。

[Matt]在 Vintage Computer Federation 论坛上找到了该项目的原理图，但使用了 PIC12F675，而不是指定的 PIC12F629。他确实提供了。他的版本十六进制文件，但不幸的是没有代码。你可以烧了它。十六进制文件或前往[原始论坛](http://www.vcfed.org/forum/showthread.php?26426-AT2XT-keyboard-converter)并抓取所有文件来制作您自己的版本。论坛提供原理图、物料清单、PCB 板布局和固件(源代码和。十六进制)，所以你只需要购买/清除零件，开始忙碌。

如果你真的觉得 31337，你可以做一个 PS/2 版本的[二进制键盘](http://hackaday.com/2016/07/20/binary-keyboard-is-the-purest-form-of-input-device/)来证明你的新适配器的使用。

[通过[危险协议类型](http://dangerousprototypes.com/blog/2017/01/12/building-an-at2xtkb-at-to-xt-keyboard-adapter-on-prototype-board/)