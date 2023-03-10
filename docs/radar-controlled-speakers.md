# 雷达控制扬声器

> 原文：<https://hackaday.com/2017/07/07/radar-controlled-speakers/>

[Scott]有一个简单的问题，他厌倦了趴在工作台上改变扬声器的音量。他需要一个能让他在更舒适的距离内轻松开关扬声器的系统。斯科特并不满足于现有的传统解决方案，他为自己的扬声器系统发明了一个雷达启动开关。

这一构建依赖于一个令人惊讶的具有成本效益的雷达模块[，它可以在 5.8GHz 的频谱上运行。在不到 10 美元的价格下，将其中一个投入到需要一些基本距离感测的项目中没什么大不了的。[Scott]决定保持简单——而不是用全脂肪微控制器来控制扬声器，而是用一个](http://www.icstation.com/microwave-radar-sensor-module-58ghz-waveband-392211mm-p-9551.html) [74HC590 IC](https://assets.nexperia.com/documents/data-sheet/74HC590.pdf) 来创建一个锁存器。每当雷达模块感应到附近有物体时，它就会触发锁闩的状态。然后，闩锁控制一个开关扬声器电源的晶体管。

总的来说，这是一个结合了现代集成雷达模块和一些非常简单的控制逻辑来创建一个功能性的建筑。当然，使用 74 系列逻辑还可以做更多的事情。休息后的视频。

 [https://www.youtube.com/embed/EIuYRhChw60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EIuYRhChw60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

