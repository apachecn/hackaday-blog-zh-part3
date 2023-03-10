# 构建自己的键盘的全过程

> 原文：<https://hackaday.com/2018/07/03/the-a-to-z-of-building-your-own-keyboard/>

我们精选了一些人，他们大胆尝试，创造了他们自己的定制键盘；在这一点上，可以肯定地说，已经有足够的信息和源代码，任何想要构建自己的开发板的人都不会有太多的问题来弄清楚如何去做。话虽如此，从头到尾全面了解一个过程还是不错的。如果没有必要，为什么要在论坛帖子和图片库中寻找碎屑呢？

[![](img/fa9c2c85be9c8628b72add3247f86d28.png)](https://hackaday.com/wp-content/uploads/2018/06/avrkbd_detail.jpg) 这正是【马顿·特罗普】的这篇文章如此有趣的原因。他带领读者经历了他的定制键盘的设计和创作的每一步[，从提出相当独特的布局到为其 AVR 微控制器编写固件。这是一本很长的读物，充满了来自众多学科的大量提示和技巧。](https://www.geekabit.nl/projects/building-a-keyboard-from-scratch/)

在寻找其他定制板的灵感后，[Maarten]使用 OpenSCAD 创建了他提议设计的 3D 模型，并在 Shapeways 打印出来。他的电子设备基于 Atmel ATMega328P，使用 vUSB 和微芯片 MCP23017 I/O 扩展器连接所有按键。最后，他在 gEDA PCB 公司设计了一款 PCB，并交付生产。作为他对细节的关注的证明，第一次尝试一切都配合得很好。

[Maarten]对最终产品很满意，但提到在未来的版本中，他希望添加 RGB 照明，并使用具有本机 USB 支持的微控制器。他还想放弃 I/O 扩展器，转而使用 Charlieplexing 来实现关键矩阵。

从不同寻常的布局到[小巧多彩的美女](https://hackaday.com/2018/02/15/arduino-keyboard-is-gorgeous-inside-and-out/)，定制键盘似乎永无止境。我们没有抱怨。