# 黑进蛙跳电视玩毁灭战士

> 原文：<https://hackaday.com/2015/12/24/hacking-the-leapfrog-tv-to-play-doom/>

几个小时后，数以百万计的新面孔儿童将会打开礼物，比如 Leap TV，这是一款面向学龄前人群的 Wii，其中有许多教育游戏。一旦他们厌倦了，还有什么比与一大群恶魔战斗来拯救地球更有教育意义的呢？是的，[米克]黑了 Leap 电视控制台来玩毁灭战士。经过一番探索，他发现 [Leap TV](http://www.leapfrog.com/en-us/products/leaptv) 是围绕四核 [nxp4330q arm7-A](http://www.insignal.co.kr/business/nxp4330) 处理器构建的，配有 1GB 内存和 16GB 闪存，而控制器则通过蓝牙 le 连接到主控制台。这对于运行 Doom 来说绰绰有余(事实上…太多了)，所以他拿出了他方便的编译器，让 [Doom](https://github.com/id-Software/DOOM) 和 [SDL](https://www.libsdl.org/) 运行起来，只做了一些小的代码修改。

这已经不是[米克]第一次被黑客攻击了:他之前曾黑过 V-Tech InnoTab，这是一款面向儿童的廉价平板电脑，说服了[制造商发布平板电脑](http://hackaday.com/2012/07/11/turning-the-innotab-into-a-linux-tablet/)的完整源代码。蛙跳会效仿吗？这还有待观察，但与此同时，[米克]的工作让我们对这个装置的内部有了一些了解。

 [https://www.youtube.com/embed/AbnhyR8NwcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AbnhyR8NwcI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

