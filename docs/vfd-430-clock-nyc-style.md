# VFD 430 时钟，纽约风格

> 原文：<https://hackaday.com/2016/01/25/vfd-430-clock-nyc-style/>

[丹尼尔]看起来他有很多时间做钟表，这对我们来说很好。对于他的最新作品，他使用真空荧光显示器(VFD)来显示小时、分钟和秒，使用 MSP430 来驱动它。

像[他最近建的模拟米钟](http://hackaday.com/2016/01/05/current-meter-shows-current-time/)，没有 RTC。相反，[Daniel]使用 430 的看门狗定时器从 430 的 32KHz 时钟产生 1Hz 中断。[Daniel]想在这个项目中尝试曼哈顿风格的板结构，所以他在打孔切割的条形板上构建每个模块，并将它们超级粘合到覆铜板上。我们不得不同意[Daniel]的观点，裸机结构很好地补充了 VFD 的美感。

[Daniel]开始避免使用 VFD 显示驱动器，但是每个段都需要+50V。他浏览了几个绘图板想法，例如在最终确定使用 [MAX6921 VFD 驱动器](https://www.maximintegrated.com/en/products/power/display-power-control/MAX6921.html)之前，使用 17 个晶体管来驱动它们。+50V 来自他建立的开环升压转换器，从 12V 逐步增加。

使用两个中断触发按钮设置时间，这两个按钮使用 TI 中的[移位寄存器示例作为起始点。所有的代码都可以在[丹尼尔]的网站上找到。休息后留下来快速演示一下时钟。](http://processors.wiki.ti.com/index.php/MSP430_Launchpad_Shift_Register)

 [https://www.youtube.com/embed/FJc-KY1ck6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FJc-KY1ck6U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

