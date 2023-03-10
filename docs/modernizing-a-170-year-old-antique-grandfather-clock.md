# 现代化的 170 岁的古董落地钟

> 原文：<https://hackaday.com/2017/11/17/modernizing-a-170-year-old-antique-grandfather-clock/>

坦率地说，当我们在提示行“[带 Arduino 内饰的古董落地钟](http://dhenshaw.net/judge)”中读到这个消息时，我们发出了绝望的叫声！但在你翻白眼、呻吟或发帖抨击之前，先看看[大卫·亨肖]那篇关于他如何花了近八个月时间致力于这一转变的惊人博文。

在你对他的资历下任何结论之前，我们必须指出[大卫]是一个王牌黑客，他已经做了很长时间的电子钟。在这个项目中，他将 1847 年的古董落地钟放入一个新的机芯中，该机芯由 Meccano 部件、步进电机、霍尔传感器、led、Arduino 和许多试验板和跳线组成，同时确保它的外观和声音尽可能接近原版。

![](img/7c65e8ba1e1edbea6017736fbf2918f0.png)他从制作一个定制的电子机械钟机芯开始，因为他在进行规划，所以 meccano、试验板和跳线都是合适的选择。热熔胶有助于保持所有跳线的位置。为了与时钟中的所有外设接口，他决定使用一组由常规 Arduino Uno 驱动的移位寄存器。与较便宜的 DS1307 或类似产品相比，较贵的 DS3231 RTC 模块可确保更高的精度。一排 RGB LEDs 充当时钟内部的信号器面板，帮助提供各种状态指示。机械运动本身经历了几次迭代，以使时间显示与指针的平滑运动一起工作。除了显示时间，【大卫】还增加了月相指示表盘。使用步进电机驱动的凸轮敲击五杆编钟，并使用单独的螺线管同时拉动和释放三个编钟锤，以产生响亮的锣声。

令人惊奇的是，他在接触到真正的落地钟之前做了所有这些，落地钟是从英国的古董钟表专家那里运到加州的，花了两个月才到达。[David]只订购了钟壳、表盘/表盘和外部零件，没有原装的内部机械装置。一旦他收到它，他的定制时钟组装需要更多的调整，以获得各种指针和表盘的正确位置。像这样一个没有典型的“滴答”声的时钟会非常蹩脚，所以[大卫]使用一对螺线管来提供声音效果，每个螺线管打开不同的持续时间来产生特有的滴答声。

八个月后，结果——命名为“法官”——相当令人满意。查看下面的视频，自己判断一下评委。如果你想看更多[大卫]的发条装置，请查看[多蒂翻转点钟](https://hackaday.com/2014/10/24/dottie-the-flip-dot-clock/)和[卷轴到卷轴钟](https://hackaday.com/2014/02/12/a-reel-to-reel-clock/)。

 [https://www.youtube.com/embed/oxTk3Q-Ah08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oxTk3Q-Ah08?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

