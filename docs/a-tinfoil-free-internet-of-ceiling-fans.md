# 一个没有锡纸的吊扇网络

> 原文：<https://hackaday.com/2018/06/08/a-tinfoil-free-internet-of-ceiling-fans/>

将所有东西放到互联网上越来越容易，因为有大量的互联网设备以及廉价而丰富的物联网模块来集成传统设备。想想可以通过智能手机控制的物联网灯泡、冰箱和洗碗机，以及无处不在的 Sonoff 模块。但是这些东西一旦上了网，他们在说什么呢？他们在背后说你什么吗？他们会把你冰箱里的东西运到国外，违背你的意愿来赚钱吗？

也许是，也许不是，但在没有锡箔头盔的情况下，保护自己的唯一方法就是建立自己的系统。[吊扇的物联网控制](http://www.microentropie.com/2018/05/ceiling-fan-controller/)是一个很好的例子，还有一个好处是大多数无线吊扇遥控器都有点糟糕。[microtropie]不喜欢走 Sonoff 路线的想法，所以他的定制控制器基于物联网的主力产品 ESP8266。有两个版本，一个用继电器切换照明和风扇负载，一个用三端双向可控硅开关。ESP 提供自己的网页进行控制，而不是使用云服务，并且能够设置风扇在预设的时间或温度自动打开和关闭。所有东西都放在靠近风扇的天花板上的一个不显眼的盒子里，但我们打赌这个盒子可以小到足以安装在风扇外壳内。

如果[microtropie]的一些代码看起来很熟悉，那可能是因为他从他的[物联网电饭煲项目](https://hackaday.com/2017/04/22/the-internet-of-rice-cookers/)中借鉴了这些代码。