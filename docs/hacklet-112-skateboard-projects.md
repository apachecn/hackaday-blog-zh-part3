# hack let 112–滑板项目

> 原文：<https://hackaday.com/2016/06/18/hacklet-112-skateboard-projects/>

滑板是一项诞生于黑客的运动。第一个用牛奶箱把旱冰鞋轮子钉在木板上的人的身份已经被历史遗忘了。那些板条箱滑板车是 20 世纪 40 年代和 50 年代的主要商品。每个人都造了自己的滑板车，所以设计也随之发展。最终牛奶箱消失了。在某些时候，冲浪者意识到他们可以使用这些带轮子的冲浪板在混凝土丛林中冲浪。事情就从那里开始了。滑板现在是一个价值数十亿美元的产业，但其核心仍然是黑客在尝试新的设计。本周的 Hacklet 都是关于滑板项目的。

[![long1](img/38f5f92f92594d9bbc4a1cb9828e2113.png)](https://hackaday.io/project/12123) 我们先从【brian.rundle】和[电长板](https://hackaday.io/project/12123)说起。[Brian]用一家 DIY 滑板网上商店的卡车和机械零件制作了他的滑板。电机是来自 HobbyKing 的无刷 outrunner R/C 平面电机。电池是脂肪种类的。Arduino Nano 提供驱动电子速度控制(ESC)的 PWM 信号。油门控制是通过射频链路使用流行的北欧 Semi NRF2401。[Brian]正专注于制造一个安全的滑板。他设计它携带两块电池，尽管每次只有一块电池在使用。他没有使用开关，而是创建了一个带有保险插头和跳线的防呆系统。每个电池都有自己的保险插头。有一个跳线，因此一次只能将一个电池连接到板上。

[![brake1](img/58869e09c6473f90703b7afdeec79eca.png)](https://hackaday.io/project/6781) 接下来是【suiram21】带[长板刹](https://hackaday.io/project/6781)。速降长板可能是一项危险的运动。在没有刹车的情况下以 40 英里/小时或更高的速度下坡会让人肾上腺素激增。[suiram21]热爱长板运动，但希望在需要的时候有一个安全的刹车。他从翁达板开始，翁达板是一种带有大直径轮子的长板。电缆驱动制动系统的 3D 打印支架。踩下踏板后面的控制杆就可以启动刹车。一根杠杆将自行车刹车片压入轮胎的内侧边缘。这将使董事会轻轻停下来。[suiram21]正在考虑在另一个车轮上增加第二个制动器，以增加制动权限。

[![speedo1](img/5e98fa366e27e9689a5100949db8087e.png)](https://hackaday.io/project/10286) 接下来我们有【edbraun】用[发明的](https://hackaday.io/project/10286)滑板测速仪。想知道他开得有多快。GPS 可以工作，但是 GPS 信号在城市里经常被屏蔽。更准确的收集速度数据的方法是直接从车轮上获取。两个小磁铁塞被放在轮子上钻的孔里。霍尔效应传感器检测到磁铁，并将数据传递给 Arduino Pro Mini。一旦计算出速度，它就被发送到蓝牙无线电。[edbraun 的] Android 手机接收数据并显示当前速度和总行驶距离。速度计及其光滑的 3D 打印外壳几乎隐藏在卡车和电路板之间。干得好[埃德布朗]！

[![josh1](img/f0f367b9c74ea9268f17f2058bcfa79a.png)](https://hackaday.io/project/13) 最后我们有 Hackaday 明矾【乔希马什】和 [EV 通勤长板](https://hackaday.io/project/13)。[Josh]在日常通勤中使用电动长板。他的项目是一个极好的概述和从头开始构建电动滑板的教程。像许多其他人一样，[乔希]利用遥控飞机无刷电机和速度控制器。驱动这些设备只需要一个 Arduino 或类似的微控制器。对于电池，[乔希]喜欢脂肪包。长型六节电池提供 22.2 伏电压，容量为 5000 毫安或以上。充足的动力为您开辟工作道路！

如果你想看到更多的滑板项目，请查看我们新的[滑板项目列表！](https://hackaday.io/list/12262)如果我错过了你的项目，不要害羞，只要[在 Hackaday.io 上给我留言](https://hackaday.io/adam)。这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！