# 魔术笔中的死错误逻辑探针

> 原文：<https://hackaday.com/2016/12/24/dead-bug-logic-probe-in-a-magic-marker/>

逻辑探针是简单而方便的工具，只需花几美元就能买到。它们可能不是最性感的测试工具，也不是最通用的，但它们有自己的位置，并且[构建自己的逻辑探针](http://yeoldetransistor.tumblr.com/post/154463437509/a-logic-probe)是了解该工具优缺点的好方法。

[Jxnblk]对逻辑探针的理解基于[Tony van Roon]的[a 电路](http://www.sentex.ca/~mec1995/circ/probe1.htm)。这个设计追溯到一个更简单的时代，并且基于从前在任何一个收音机小屋都很容易拿起的组件。逻辑部分以经典 14 引脚 DIP 格式的古老的 7400 四路 2 输入与非门为中心。门电路分别点亮高逻辑电平和低逻辑电平的 led，单触发配置的 555 定时器芯片充当脉冲展宽器来捕捉瞬变。DIP 包有助于快速和肮脏的[“死虫”构造](http://hackaday.com/2016/05/04/getting-ugly-dead-bugs-and-going-to-manhattan/)，整个东西正好适合一个废弃的标记笔。

![dead-bug-logic-probe-in-marker-body](img/ee7afa078ce9d6cc27df99d14e8211af.png)

对于一个有用的工具来说，这是一个简单的构建和良好的外形，但对于像旧注射器这样更薄的封装来说，你可能不得不使用 SMD 元件。当你从简单的逻辑探针毕业时，你可能想看看[这个智能探针](https://hackaday.com/2014/05/29/tiq-probe-is-more-logical-than-most/)的能力。