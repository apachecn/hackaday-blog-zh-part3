# 敲三下你的脚后跟，叫辆出租车回家

> 原文：<https://hackaday.com/2017/10/17/click-your-heels-thrice-hail-a-cab-home/>

如果《绿野仙踪》中的多萝西在 2017 年醒来，脚上穿着一双神奇的红宝石拖鞋，她可能会相信自己醒来时是在一个神奇的世界里。但是现代人需要更多的魔力来打动他们。就像[穿着这双优步红宝石拖鞋敲三下脚跟回家](https://www.newscientist.com/article/mg23431273-000-do-try-this-at-home/)。[Hannah Joshua]被她的雇主指派去建造一个古怪的创客项目。当一个朋友抱怨在辛苦工作一天后很难叫到出租车时，她有了一个想法。

[Hannah]从红宝石色的厚底拖鞋和高跟鞋开始，以便留出空间来塞下所有的魔法灰尘，呃，电子元件。最初的计划是使用带有 GSM/GPS 屏蔽的 Arduino，但这需要一个单独的 SIM 卡和鞋子的数据计划。相反，她选择了通过蓝牙连接智能手机的 [1Sheeld](https://1sheeld.com/) 。1Sheeld 可以访问智能手机的所有传感器，包括 GPS 和数据连接。Arduino 和 1Sheeld 放在鞋头部分的空腔中。9 V 电池放在鞋跟的另一个空腔中，那里也安装了一个激活开关。三个发光二极管指示何时鞋被激活，何时接受轿厢请求，何时轿厢上路。

这是她第一个 Arduino 项目中的一个，代码是基本的，但它完成了工作。它向优步的 API 发送一个 http 请求来请求 cab。目的地是硬编码的，所以拖鞋只允许你从你当前的位置到达任何被编程的目的地。GitHub 库提供了代码，以及一些关于构建的附加信息。[Hannah]还添加了注释，解释了一些设计选择，以及如果您计划制作一双这种魔法拖鞋时需要注意的事项。

几年前，当 [1Sheeld](https://hackaday.com/2013/10/29/1sheeld-uses-your-smartphone-as-an-arduino-accessory/) 推出时，我们报道过它，如果你得到了一个，试着建造这个[手动开门器](https://hackaday.com/2016/09/05/hand-waving-unlocks-door/)。

 [https://www.youtube.com/embed/lc6yP_4Sn-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lc6yP_4Sn-M?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

