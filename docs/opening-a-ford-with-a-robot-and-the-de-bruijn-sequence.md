# 用机器人和德布鲁因序列开一辆福特

> 原文：<https://hackaday.com/2018/06/18/opening-a-ford-with-a-robot-and-the-de-bruijn-sequence/>

福特 Securicode，或所有型号的福特汽车和卡车上都有的无钥匙进入键盘，首次出现在 1980 年的雷鸟上。尽管它最常见于高端车型，但它也可以作为福特在美国销售的最便宜的汽车嘉年华 S 的一个选项，售价 95 美元。Doug DeMuro 喜欢它。它也是一把锁，这意味着它随时可以被利用。当然，有人可以制造一个机器人来打开这把锁。[事实证明，这很容易](https://hackaday.io/project/27445-five-finger-code-finder)。

这个建筑的电子和机械部分非常简单。一个压克力框架在键盘上装有五个螺线管，这个压克力框架用磁铁固定在汽车上。还有第二个大型原型板连接到这个丙烯酸框架，加载了 Arduino、字符显示器和 ULN2003 来驱动电阻。到目前为止，你所期待的通过键盘解锁汽车的“机器人”都具备了。

这个版本的真正诀窍是让这个电子开锁器快速且易于使用。这个项目的灵感来自于[【Samy Kamkar】为车库门开启器设计的 OpenSesame 攻击](http://samy.pl/opensesame/)。在这个项目中，[Samy]没有通过发送一个接一个的代码来强行编码；(蹩脚的)车库门开启器只看遥控器发来的最后一个 *n* 数字，发错码也不罚。在这种情况下，可以使用[一个 De Bruijn 序列](https://en.wikipedia.org/wiki/De_Bruijn_sequence)来大大减少暴力破解每个代码所需的时间。这个机器人只需要测试 3125 个代码，而不是按顺序测试成千上万个不同的代码，这应该只需要几分钟。

现在这个项目的创造者正在对这个福特破解机器人进行最后的润色。代码中有一个小错误，通过[将 De Bruijn 序列视为循环](https://hackaday.io/project/27445-five-finger-code-finder/log/148053-found-a-bit-of-a-bug-an-easy-fix-but-hard-to-find)得到了解决，但现在 1993 年的福特金牛座旅行车变得更加毫无价值只是时间问题。