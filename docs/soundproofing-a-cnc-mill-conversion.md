# 隔音一数控轧机转换

> 原文：<https://hackaday.com/2018/05/10/soundproofing-a-cnc-mill-conversion/>

Proxxon MF70 是一台漂亮的台式铣床，有许多有用的附件，非常适合黑客在自己的工作室里拥有一台。但它每分钟 20000 转的转轴会引起相当大的噪音，并会让邻居面红耳赤。此外，你如何在你的家庭作坊里使用铣床，而不使整个区域布满金属屑和锯屑？为了解决这些问题，[Tim Lebacq]正在对他的数控铣床改装进行隔音处理。

为了达到他的隔音目标，他显然必须首先将[手动 MF70](https://www.proxxon.com/en/micromot/27110.php) 转换为数控版本。这相当简单，多年来已经在这台机器和类似的机器上以许多不同的方式完成了。[Tim]坚持使用久经考验的控制器解决方案，包括一个 Raspberry Pi、一个 Arduino Uno 和一个 grbl shield 三明治，三个 NEMA17 电机采用步进电机驱动器。电子设备安装在旧电源的回收金属盒内。由于 Proxxon MF70 已经设计为接受 CNC 转换包，安装电机和限位开关非常简单，便于[Tim]进行升级。

隔音箱是他面对未知领域的地方。盒子本身是由木质框架和刨花板制成的。一对带插销锁的抽屉滑轨用于垂直向上打开的前门。他还加入了一些通过 Raspberry-Pi 控制的 RGB 条，用于环境照明和状态指示。但是为了隔音，他尝试了各种材料和技术。最终，他选定了一层泡沫塑料，上面还有一层“气泡包装”！看起来气泡包装的不平整表面在降低声音方面非常有效——至少对他的耳朵来说是这样。时间和邻居会证明一切。

也许高密度的“声学泡沫”板会更有效(类似于“鸡蛋箱”风格的泡沫板，只是密度更大)？然而，当使用这种隔音泡沫时，清洁盒子的内部可能是一个很大的挑战。你会选择什么材料来建造这样一个隔音的盒子？请在下面的评论中告诉我们。回到很多年前，我们已经发布了关于 Proxxon MF70 的这个“[便携式数控铣床](https://hackaday.com/2012/12/28/a-portable-cnc-mill/)和一个“[铣床到数控铣床的转换](https://hackaday.com/2013/10/25/converting-a-mill-to-cnc-2/)”。看起来像是黑客中受欢迎的机器。