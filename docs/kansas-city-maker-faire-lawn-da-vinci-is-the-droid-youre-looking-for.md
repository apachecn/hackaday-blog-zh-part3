# 堪萨斯城创客大会:劳恩·达芬奇就是你要找的机器人

> 原文：<https://hackaday.com/2016/07/17/kansas-city-maker-faire-lawn-da-vinci-is-the-droid-youre-looking-for/>

夏天现在正如火如荼，这意味着每周修剪一次草坪开始变得过时了。那么为什么不造一个机器人来帮你呢？这就是布莱克·霍奇森所做的，他从未如此开心过。他只花了几个星期的时间在当地的一个创客空间。

[布莱克]在今年的堪萨斯城创客节上展示了草坪达芬奇。他在 hammer space 的拐角处有自己的摊位，所有的东西都是在那里组装的。[Blake]从车库销售的标准推式割草机开始，并使用 OnShape 围绕它设计了一个框架。这个框架是用角铁制成的，所以很结实，他可以骑在上面。我们说，人各有志。轮子和马达来自一辆轻便摩托车，与结实的车架相匹配。这些电池由两个串联的 12v 汽车电池供电。他用遥控飞机控制器开着它在他的院子里转。

[![lawnmower guts](img/4e8868bd9a1b1c7a14052922bd9d8150.png)](https://hackaday.com/wp-content/uploads/2016/06/lawnmower-guts.jpg) 劳恩达芬奇的脑力来源于两台 Arduino Pro Minis 和一个树莓派。一个 Arduino 通过遥控器**控制电机和遥控信号。**另一个运行一些额外的切断开关，让达芬奇远离草坪上的麻烦。

那这个锉刀是干什么用的？现在，它可以将连接在支架上的网络摄像头的视频传输回他的手机。[Blake]说他的网络摄像头有一些延迟问题，所以他未来可能会有一副无人机比赛护目镜。他还计划增加一个 GPS 记录器，并实现部分割草的自动化。

现在，关于那些断路开关:有几个。在一台遥控旋转的郊区死亡机器上，你可能不会有太多这样的东西。草坪达芬奇将停止放牧，如果它走出了遥控器的范围或如果遥控器被关闭。[Blake]还在遥控器的一个按钮上连接了一个专用的切断开关，第四个在一个单独的钥匙链上。

草坪达芬奇是[布莱克]用来展示 [KC Proto](http://www.kcproto.com/) 的可能性的许多示例项目之一，他创办了这家公司，通过提供设计解决方案和原型制作协助来帮助当地企业实现他们的想法。在抽烟的间隙，[布莱克]把电池放在涓流充电器上。如果你自己制造机器人割草机，你可能会考虑制造燃气和太阳能混合动力车[。](https://hackaday.com/2013/04/07/solar-powered-robot-mows-your-lawn-while-you-chill-indoors/)