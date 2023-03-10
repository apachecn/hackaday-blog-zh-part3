# 灯丝厚度传感器，它们是什么，有什么用途？

> 原文：<https://hackaday.com/2016/02/05/filament-thickness-sensors-what-are-they-and-what-are-they-good-for/>

我相当好地跟上了 3D 打印的趋势。有一天，我的朋友提到灯丝厚度感应已经被添加到最新版本的马林固件中。我不知道那是什么，但听起来确实很酷。我必须了解更多。

在工业环境中，[灯丝是通过将熔融塑料以一定的速度拉入冷却池中而制成的](http://makezine.com/2015/02/11/how-it-is-made-3d-printing-filament/)。[2.85 毫米灯丝和 1.75 毫米灯丝](http://hackaday.com/2015/09/29/3d-printing-has-evolved-two-filament-standards/)的喷嘴实际上尺寸相同，但灯丝在离开喷嘴时或多或少会被拉伸。通过平衡这三个变量，挤出机可以生产任何尺寸的长丝。像任何机械系统一样，它需要不断调整以保持平衡。这通常是通过在灯丝冷却后用激光测量灯丝，然后将信息反馈到系统中来完成的。更好的灯丝制造商有多个激光器和非常快速的反馈回路。一些[最好的](http://atomicfilament.com/collections/opaque-pla-filaments-1/products/black-pla-filament?variant=2948449345)在灯丝的任意两点之间提供±0.04 毫米或更小的厚度变化。有些最差的误差较大，如+/-10 毫米。由于塑料以固定的线速度送入挤出机，这使得每秒钟从喷嘴中流出的塑料量发生变化。在最好的情况下，我们看到挤出的塑料体积有 4.41%的变化。最糟糕的时候，我们开始看到 10.51%或更多。

![FIlament variation showing up as a cosmetic defect.](img/8f84fb6da8160ab1fffcfb057a2ad169.png)

Filament variation showing up as a cosmetic defect.

打印机是哑的。它在假设得到绝对完美的细丝的情况下工作。所以当它多了 10.51%的塑料时，它只是把它推出去，继续它的生活。然而，如果灯丝偏离得足够远，这实际上会在印刷品上显示为可见的缺陷。或者在更坏的情况下，由于塑料的过度挤压或挤压不足而导致印刷失败。

那么，灯丝厚度传感器如何解决这个问题呢？为了开始理解，我们需要看看软件是如何处理灯丝的。当切片机为 3D 打印编译 g 代码时，它会计算出每移动一毫米就沉积一定宽度和高度的塑料珠所需的塑料量。那是一口。例如，当打印 0.2 毫米层的打印机移动 1 毫米时，它希望放下 1.0 毫米长 x 0.4mm 毫米宽 x 0.2mm 毫米高的卷。被推入喷嘴的长丝每毫米的体积由长丝的直径决定。

![(\pi (radius_{filament})^{2}*length_{filament extruded})=volume](img/478d7b75dfb8e7181f3ca52abb6a0345.png)

每毫米英寸长丝的体积。

![(layer_{height}*layer_{width}*length_{move}) = volume](img/835312ceb5803944595c07d498e04bb4.png)

我们试图平衡的等式。

我们的目标是将厚度传感器集成到这些功能中，看看厚度传感器在做什么。这是一个线性方程，所以这里没有什么花哨的。现在，移动的层高度、层宽度和长度分别由设置和模型几何决定。这些是固定的数字，所以我们不关心它们。这样我们就得到了长丝的直径和挤出长丝的长度。如前所述，通常假设灯丝的直径是固定的。因此，所有的软件必须计算的是，在 x 和 y 方向上，每毫米的组合运动需要挤出的细丝长度，这样我们的体积就匹配了。

但是，我们知道其中一个变量实际上也在每毫米变化。灯丝直径！所以现在我们有一个问题。如果细丝直径一直在变化，我们的方程就永远不会平衡！为了解决这个问题，我们可以在等式中加入一个乘数。因为我们不能控制灯丝的宽度，所以我们不能修改这个值。然而，如果我们知道细丝的宽度，并且我们知道它应该是什么值，我们就可以改变挤出细丝的长度。这是因为与长丝不同，我们可以控制驱动挤出机的步进电机。这个值被称为挤压乘数，它的确定是厚度传感器的全部内容。

因此，灯丝传感器所做的只是测量灯丝的当前直径。它将预期直径除以刚刚测量的值，得到一个简单的百分比。它将这个数字反馈到我们的系统中，作为挤出机的倍增器，并根据需要减慢或加快步进电机的速度。很简单。

 [![The ideal filament the printer thinks it is seeing.](img/aa1c5829bcee8543e42637da38761df4.png "perfect-filament")](https://hackaday.com/2016/02/05/filament-thickness-sensors-what-are-they-and-what-are-they-good-for/perfect-filament/) The ideal filament the printer thinks it is seeing. [![The printer is unable to compensate for the variations.](img/c84f1096a7b84d58826ec70642c1691e.png "bad filament no multiplier")](https://hackaday.com/2016/02/05/filament-thickness-sensors-what-are-they-and-what-are-they-good-for/bad-filament-no-multiplier/) The printer is unable to compensate for the variations. [![By adjusting with the extrusion multiplier the printer is able to approximate perfect filament.](img/1c33984cd95196ecc0e5bc59be566fc3.png "perfect-again")](https://hackaday.com/2016/02/05/filament-thickness-sensors-what-are-they-and-what-are-they-good-for/perfect-again/) By adjusting with the extrusion multiplier the printer is able to approximate perfect filament.![2016-01-26_00h08_00](img/de1752b5873f87c8bef6c9f3162856e0.png)

传感器上的阴影来自【无条件】的变化。

现在有几个厚度传感器正在被摆弄。第一，据我所知；如果我在评论中说错了，请告诉我。他现在已经是第三个版本了。该传感器的工作原理是当灯丝经过时，在光学传感器上投射一个影子。固件然后计算像素，并向后工作以获得直径。这个值被发送到打印机上的 Marlin 固件，由它完成其余的工作。就像开源社区中常见的奇妙现象一样，不久其他人也开始着手解决这个问题。通过在传感器上投射更多的阴影来改进这个想法。这项技术仍然是全新的，但看看它能带来什么好处会很有趣。

现在下一个问题来了，“值得用厚度传感器升级我的打印机吗？”如果你通常运行差的细丝，或者如果你[挤出你自己的](http://hackaday.com/2013/03/05/finally-a-machine-that-makes-cheap-3d-printer-filament/)，是的。目前的传感器只能测量+/-0.02 毫米。所以对于最好的灯丝，你不会真正看到差异，但对于更差的东西，你可能会看到差异。莱曼长丝挤出机的最新固件，用于制造您自己的长丝，也支持这些传感器，让您像工业机器一样反馈到您的生产系统。总而言之，这是 3D 打印机领域一个非常有趣的发展。