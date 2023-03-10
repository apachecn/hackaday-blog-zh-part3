# 锯掉键盘

> 原文：<https://hackaday.com/2017/09/18/sawed-off-keyboard/>

你曾经不得不把一件家具切成两半，然后把它搬到一个新的地方吗？你的的确如此，不得不把组合沙发的较长部分切成两半，才能放进高层公寓。这就是[查尔斯]' [锯掉键盘](https://hackaday.io/project/27236-saw-your-keyboard)立刻让我们想起的。这听起来很疯狂，但同时也很聪明。

[![](img/0b4d6e6321f10633f1569cb09646765e.png)](https://hackaday.com/wp-content/uploads/2017/09/4403481505155020532_thumbnail.png) 在【Charles】的案例中，他想要一个按键可定制的小键盘，一次按键就能完成剪切、复制和粘贴等常见操作，在 Windows 中通常是 ctrl-X、ctrl-C 和 ctrl-V。为此，他从全尺寸键盘上锯下了数字键盘。他还锯掉了 QWERTY 键盘左边的一端，并将其粘在键盘的开口端。

电路板太宽，不适合他的新键盘，但他无法将键盘的按键连接到电路板上。因此，他做了任何有自尊的黑客都会做的事情，他在有可管理数量的迹线的地方切割电路板，留下一部分可以放在键盘内，另一部分可以用几根电线连接迹线。最后，他从 PS/2 键盘开始，但是他想要 USB 输出和可编程性。因此，他将 PS/2 线重定向到 Arduino 兼容的 Pro Micro，并编写了一些转换代码，你可以在他的 [GitHub](https://github.com/CharlesVanDen/sawboard) 上找到。

我们还能对键盘做哪些改变？[Shrodingers_Cat]将他的与一些 DVD 壳盖结合起来，想出了一个[脚踏板，供他的脚](https://hackaday.com/2016/03/27/turning-a-keyboard-into-a-pedal-board/)使用。鉴于数字键盘上的按键是多余的，[Kipkay]将其用作[，而不是](https://hackaday.com/2015/07/18/secret-keyboard-stash/)藏贵重物品的地方。