# 一个老式的单晶体管 LED 闪光灯

> 原文：<https://hackaday.com/2016/10/17/a-vintage-single-transistor-led-blinker/>

[Eric Wasatonic]有一盒 SWB2433 晶体管，但他对其了解甚少。为了发现它们的特性，他启动了曲线跟踪器，将这些晶体管与更常见的晶体管进行比较。他注意到 SWB2433 表现出负电阻，而 2n3904 的类似曲线则没有。然后，他反向偏置两个晶体管:2n3904 上的负电阻区域小于 SWB2433，但它确实存在，2n2222 的负电阻区域更大。利用这一知识，[他开发了一种使用负偏置晶体管的张弛振荡器电路](https://www.youtube.com/watch?v=rpGOKGrcpAk)。

他用一个晶体管、一个电阻和一个电容描述了电路，以及这些元件如何影响振荡器产生的锯齿波的频率。[Eric]使用振荡器构建了一个简单的 LED 闪光灯，并展示了当他改变晶体管并调整电压或电阻时会发生什么。他还展示了作为音调发生器的电路，并通过用电位计代替电阻来调节音调。然后，为了好玩，他修改了电路，将振荡器显示为调幅发射机。休息之后看看他的视频。

当然，[Eric Wasatonic]并没有想出这个主意(他在视频描述中链接到这个简单的 LED 闪光灯电路页面),但是[Eric]向我们展示了他发现晶体管负电阻的过程和电路的结果。尽管还有其他的[方法](http://hackaday.com/2016/10/13/blinking-an-led-extreme-edition/)来使 LED 闪烁，还有其他的[方法](http://hackaday.com/2015/02/04/logic-noise-sweet-sweet-oscillator-sounds/)来制造振荡器，但是【埃里克】的电路还是非常简单的。

[谢谢 fede.tft]

 [https://www.youtube.com/embed/rpGOKGrcpAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rpGOKGrcpAk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

