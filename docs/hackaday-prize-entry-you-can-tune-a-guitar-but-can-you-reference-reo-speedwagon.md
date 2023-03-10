# Hackaday 奖参赛作品:你可以给吉他调音，但你能参考快速马车合唱团吗？

> 原文：<https://hackaday.com/2017/09/17/hackaday-prize-entry-you-can-tune-a-guitar-but-can-you-reference-reo-speedwagon/>

就一会儿，让我们做一个基于工程的思维实验。让我们设计一个吉他调音师。首先，您需要一个 1/4”输入和一些运算放大器来将该信号输入微控制器。在微控制器中，您将进行一些 FFT 运算。如果你真的很喜欢，你会有一些查找表和一个接口在 A440，也许是 A430 和 C256 之间切换，如果你是一个超级书呆子。界面非常简单——只需使用一个七段显示屏和几个发光二极管来告诉用户他们所在的音符和音高。总而言之，这个设计并没有那么难。

现在让我们为盲人音乐家设计一个调音器。这让事情变得更有趣了。这种 LED 界面是行不通的，你必须找到一种更好的方式来告诉音乐家他们在音高上。这是[【pepi jn】的无障碍吉他调音师](https://hackaday.io/project/26255-accesible-guitar-tuner)的想法。它入围了 Hackaday 辅助技术奖的决赛，这是一个非常有趣的问题。

大多数[Pepijn]的调谐器是你所期望的——微控制器和 FFT。微控制器是一个 ATMega，对于一个简单的吉他调音器来说已经足够了。这里真正的诀窍是接口。根据参考频率调制来自吉他的输入。吉他和这个参考频率之间的差异然后被转换成滴答声并通过耳机播放。更少的滴答声意味着吉他更接近合拍。

这是非常适合 Hackaday 奖辅助技术轮的项目之一。这是一个定义极其简单的问题，有点容易构建，而且非常有用。这并不意味着[Pepijn]没有问题——他在吉他的信号水平方面遇到了很多问题。他在寻求一些帮助，所以如果你在阅读信号方面有一些见解，从微小的压电到活跃的亨巴克，给他一些建议。

The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)