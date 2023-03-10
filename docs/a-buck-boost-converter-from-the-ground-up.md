# 一种全新的升降压转换器

> 原文：<https://hackaday.com/2016/11/22/a-buck-boost-converter-from-the-ground-up/>

从 DC 到 DC 的转变经历了漫长的过程。曾经由机电振动器和变压器组成的东西，现在已经缩小到一张邮票大小的 PC 板，在易贝只需花上几美元就能买到。那么，为什么[要推出自己的降压-升压转换器呢](http://www.instructables.com/id/DIY-BuckBoost-Converter-Flyback/)？也许是因为有时候最好的学习方法是实践。

说到清晰简洁的解释，[GreatScott！]您是否已覆盖。我们[最近在他的](http://hackaday.com/2016/10/30/primer-on-servos-hits-all-the-basics/)[电子基础](https://www.youtube.com/playlist?list=PLAROrg3NQn7cyu01HpOv5BWo217XWBZu0)系列的一个视频中报道了，但下面的视频更深入地涵盖了 DC-DC 转换这个稍微高级一点的话题。【GreatScott！]描述降压转换器和升压转换器如何作为独立实体工作，以及如何集成到同相降压-升压转换器中。他进一步将该电路简化为反相降压-升压电路，并着手解释该电路的局限性。通过增加一个运算放大器来提供反馈以控制 ATtiny85 的占空比，降压-升压转换器克服了其局限性，无论负载或电源电压如何，都能保持稳定的设定点。

如果你想将 DC-DC 转换理论付诸实践，这是一个很好的入门项目。对于老手来说也是很好的复习，大部分【GreatScott！】的视频。它们值得一查。

 [https://www.youtube.com/embed/ZiD_X-uo_TQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZiD_X-uo_TQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

