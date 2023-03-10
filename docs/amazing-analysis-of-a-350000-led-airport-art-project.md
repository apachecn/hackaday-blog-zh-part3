# 一个 35 万 LED 机场艺术项目的惊艳解析

> 原文：<https://hackaday.com/2016/05/05/amazing-analysis-of-a-350000-led-airport-art-project/>

在你尖叫“不是黑客”之前，先看几分钟这个拆机视频。这个 48 分钟的一次性艺术品的详细预演展示了项目的每个方面:每个需求、设计决策、实现挑战和错误。一些值得注意的细节:

*   1 米宽的 PCB(都是一块！)
*   35 万个白色发光二极管
*   碳纤维外壳
*   12 位分辨率(TLC5973)的单线串行总线(与 WS2812 不同)
*   定制电缆测试夹具、PCB 测试夹具和测试模式
*   生产中静电放电问题的探讨

人们并不经常看到像这样的专业项目被拆除，除了它是一件美丽的艺术品之外，这里还有很多值得学习的东西。查看更多关于希思罗机场鱼子酱馆“应急”项目的信息，以及令人惊叹的图片和视频。

如果你正在考虑如何用 12 位灰度控制 350，000 个单独的 led，并让它看起来平滑，请检查一下 [megascroller](http://hackaday.com/2014/06/05/the-megascroller-for-video-games-in-the-round/) 背后的处理器要求，它只能处理 98，000 个 led。最近，我们问[多少个 led 太多了](https://hackaday.com/2016/03/12/how-many-leds-are-too-many/)，答案是比 350k 低很多。

 [https://www.youtube.com/embed/9Qlmywxjau0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9Qlmywxjau0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

