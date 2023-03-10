# 电子浮阀保持马的脚干燥

> 原文：<https://hackaday.com/2015/11/05/electronic-float-valve/>

[Bob]建造了这个简单的装置，它可以被最好地描述为[电子浮阀](http://makingstuff.info/Projects/15/WaterShutOff.aspx)。他浪费了农场周围满溢的水槽和水桶中的大量水。他通常会将软管放入容器中，打开水阀，然后继续工作。等他想起来回来的时候，这个地区已经被洪水淹没了。很明显，解决一个问题有许多不同的方法。例如，一个简单的机械浮阀可能会工作，但它对马不友好，很快就会损坏。

电子设备是毫不掩饰的最小化。ATtiny85 通过普通的 NPN 晶体管控制继电器。继电器依次开关电磁阀。一个按钮告诉微控制器开始水流，当水位足够高，触及两个软管夹时，微控制器再次关闭水流。

这里正在进行一些贫民区工程。电子设备由 9V 电池驱动，尽管[Bob]使用的继电器和电磁阀的额定电压都是 12V。他甚至没有使用任何形式的电压调节，而是用电阻分压器来降低电压。(我们想知道电池的长期寿命。)

他在 perf 板上构建了所有这些，并将其塞在一个小外壳中，其中两根电线用于液位传感器，另外两根用于螺线管，它似乎可以工作。查看下面的视频，其中[Bob]展示了他的身材。

虽然有些人可能会指出这个版本的许多缺点，但[Bob]找到了一个适合他的解决方案。有时候，正确的解决方案就是你手头上的东西，我们很高兴他正在破解并分享他的工作。看看这个[无线水位传感器](http://hackaday.com/2015/02/13/wireless-water-level-sensor-from-pvc-pipe/)他前段时间做的。

 [https://www.youtube.com/embed/sbQfBndbXbw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sbQfBndbXbw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

