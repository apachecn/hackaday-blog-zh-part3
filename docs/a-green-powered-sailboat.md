# 绿色动力帆船

> 原文：<https://hackaday.com/2016/04/25/a-green-powered-sailboat/>

无人驾驶飞机布满天空，地狱之火如雨般落在下面毫无防备的平民身上。自动驾驶汽车造成的事故只有碳基司机的一半。自动驾驶汽车是未来，不管这个未来有多黯淡。有一样东西我们还没怎么见过，那就是自主海洋交通工具，无论是潜艇、气垫船还是帆船。这正是[silvioBi]为了参加 Hackaday 大奖正在建造的东西:[一艘将往返于意大利最大的湖泊](https://hackaday.io/project/10652-green-powered-sailboat)水域的帆船。

每艘船都需要船体，但这个项目需要更多，从电子设备到太阳能电池板到传感器。幸运的是，选择船体就像前往易贝一样简单。[silvio]为€40 挑选了一个玻璃纤维船壳，它既适合他的需要，也适合他的工作台。

电子设备有点棘手，但基本计划是用太阳能电池板覆盖甲板，并使用包括 GPS、IMU 和风速计在内的一些传感器来驾驶这艘帆船绕湖行驶。制造一辆自动驾驶汽车是一项艰巨的挑战，对于电子设备，[silvio]有一个锦囊妙计:[他正在使用冗余电子设备](https://hackaday.io/project/10652-green-powered-sailboat/log/36405-redundant-sailing-system)。所有的传感器都是通过 I2C 总线连接的，那么为什么不把两个微控制器放在总线上成为主从配置呢？这不会增加太多质量，考虑到 T2 机器人帆船比赛 T3 背后的一些团队存在的问题，有一点冗余并不是一件坏事。

The [HackadayPrize2016](http://hackaday.io/prize) is Sponsored by: [![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](http://hackaday.io/atmel)  [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](http://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](http://www.digikey.com/)  [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](http://supplyframe.com/)