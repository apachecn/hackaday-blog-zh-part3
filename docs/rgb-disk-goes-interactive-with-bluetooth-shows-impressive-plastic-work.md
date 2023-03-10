# RGB 磁盘与蓝牙进行交互；展示了令人印象深刻的塑料作品

> 原文：<https://hackaday.com/2018/03/11/rgb-disk-goes-interactive-with-bluetooth-shows-impressive-plastic-work/>

[smash_hand]有一个明确的目标:一个巨大的、毫无特色的白色塑料盘，边缘隐藏着 RGB LEDs 灯。那是什么呢？一个大装饰品，可以发出任何颜色或令人神往的混合颜色。这件物品的唯一目的是成为柔和发光图案的框架，以供欣赏。这个磁盘可以通过一个简单的智能手机应用程序来控制，该应用程序通过蓝牙进行通信，允许任何人(或者理论上任何 T2 的东西)玩这个显示器。

[![](img/0b26880e8e829e60059cfbe50e11e4cf.png)](https://hackaday.com/wp-content/uploads/2018/03/rgb-disk-anim-square.gif) 光盘由 1/4″透明塑料制成，[smash_hand]称之为有机玻璃，但也可能是丙烯酸或聚碳酸酯。【smash_hands】描述了切圆过程中的一些试错；先用一些三合一的油作为切削液进行锯切，然后用带锯切割出最终的形状。

这把锯的边缘很粗糙，所以用玻璃抛光剂抛光。这恢复了边缘照明技术所需的光学特性。光盘背面经过打磨，然后漆成白色，RGB LEDs 灯沿边缘均匀分布，指向内部。

在这样的项目中，物理构建几乎总是最困难的部分— [实现 led 的良好扩散](https://hackaday.com/2017/04/25/ask-hackaday-what-about-the-diffusers/)是我们经常谈论的话题。[smash_hands]的工作令人印象深刻，而且从来不会有任何“热点”出现在您眼前。有了这一点，电子设备组装起来就容易多了。带有 HC-05 蓝牙适配器的 Arduino 分别负责驱动 led 和无线通信。一个木架之后，整个事情就准备好了。

[smash_hands]为任何感兴趣的人提供了类似于[线路图和智能手机应用](https://www.fork20.xyz/rgb20.html)的细节。还有 Arduino 程序，但有趣的是，它只有汇编版本或原始版本。十六进制文件。下面嵌入了一个运行中的磁盘视频。

 [https://www.youtube.com/embed/uBKDtne5SQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uBKDtne5SQE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[让 LED 照明互动](https://hackaday.com/2017/01/31/an-awesome-interactive-led-table/)有许多不同的形状和形式，正如上面的圆盘所示，变换颜色图案可以令人愉快地放松。