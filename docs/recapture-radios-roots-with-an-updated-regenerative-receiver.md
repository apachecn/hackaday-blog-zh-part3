# 用更新的再生接收器重新捕捉无线电的根源

> 原文：<https://hackaday.com/2017/01/19/recapture-radios-roots-with-an-updated-regenerative-receiver/>

水晶收音机曾经是业余爱好电子产品的“入门药”。问题是，一个用铁丝包着的燕麦片纸盒、一枚安全别针和一片剃须刀片只能完成这么多事情。添加一些组件和探索再生电路可能会更有吸引力，这就是这个简单的试验板再生无线电的用武之地。

有时是简单的概念能抓住想象力，重温经典是一个很好的方法。基本上是重复了[阿姆斯特朗]1912 年的原始再生设计，[冯纳赫特]在使用玻璃的地方使用了硅，但原理是一样的。一小部分放大的射频信号通过铁氧体棒上的附加线圈反馈到调谐电路，该线圈充当接收器的天线。正反馈进一步放大 RF，锗二极管包络检波器解调信号，音频传递到一个简单的运算放大器级，用于驱动耳机。

该电路适合无焊试验板，甚至是使用[死虫或曼哈顿布线](http://hackaday.com/2016/05/04/getting-ugly-dead-bugs-and-going-to-manhattan/)的字面试验板结构，它邀请实验，看起来很有趣。掌握模拟和射频概念总是一件乐事。

[通过[遥控/电子](https://www.reddit.com/r/electronics/comments/5nj6qw/regenerative_am_radio_on_a_breadboard/)