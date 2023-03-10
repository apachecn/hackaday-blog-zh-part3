# 齿轮时钟使用步进电机

> 原文：<https://hackaday.com/2016/04/24/gear-clock-uses-stepper-motor/>

[Rjeuch]喜欢他在互联网上看到的一个木制时钟，但齿轮是用专有软件工具生产的。于是他[打造了自己的](http://www.instructables.com/id/Wood-Gear-Clock-With-Stepper-Motor-Drive/)版本。然而，与最初的不同，他选择使用步进电机来驱动指针。

时钟的齿轮不只是为了展示，邮报很好地解释了齿轮如何工作，你如何定制它们，以及它们如何配合。时钟的电子设备依靠 Arduino。

当然，Arduino 的问题是时基并不总是足够好来长时间保持时间。为了解决这个问题,[Rjeuch]使用了 ChronoDot，这是一种实时时钟，使用温度补偿，并声称每年精确到一分钟。

当然，没有一个计划会一帆风顺。由于糟糕的步进模式规格，时钟的原始版本在一夜之间获得了时间。虽然踏步机声称有 1:64 的减速齿轮，但实际比率并不精确([Rjeuch]估计为 1:63.876。他采取的措施值得一读。

你可以在下面看到这个时钟的视频。当然，我们已经见过很多其他的[钟](http://hackaday.com/2016/02/12/frickin-amazing-clock/)。[其中一些](http://hackaday.com/2016/01/11/3d-printed-tourbillon-clock/)甚至让这个看起来很简单。

~~https://www.youtube.com/watch?v=HURoEW2KiY8~~