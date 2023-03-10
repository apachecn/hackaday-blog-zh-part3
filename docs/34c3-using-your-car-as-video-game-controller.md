# 34C3:用你的车作为视频游戏控制器

> 原文：<https://hackaday.com/2017/12/30/34c3-using-your-car-as-video-game-controller/>

尽管有人类司机的存在，但现代汽车是由电脑控制的。在混沌通信大会上的演讲中，[Guillaume Heilles]和[P1kachu]展示了控制汽车电脑的潜力。这当然会导致模仿 Xbox 控制器并使用汽车玩电脑游戏的自然结论。

他的研究受到这样一个事实的限制，即他们唯一能接触到的汽车是[P1kachu]家庭不同成员的日常司机，这意味着所有的修补必须严格是非破坏性的。尽管如此，他们取得了令人印象深刻的成果，并提供了逆向工程的伟大介绍。

[P1kachu]使用 RasPi 和 OBD-II 适配器访问汽车的 CAN 总线，并以快速概述协议开始演示。然后，他简要介绍了他遇到的安全措施，这些措施是可选的，不同制造商之间的实施差异很大。他第一次访问 CAN 总线的尝试被一种挑战-响应算法成功阻止。然而，他母亲的敞篷车没有提供这样的障碍，获得访问权限允许他将方向盘和踏板的位置映射到游戏控制器，使用汽车玩视频游戏。

![](img/f59c79602799889c82312229270b00b4.png)

在此之后，[Guillaume]介入并带领我们拆卸一个插入 OBD-II 端口的小工具，并声称通过重新编程 ECU 为您的汽车里程数做了惊人的事情。该设备没有特定的品牌，在看到不同制造商实现协议的方式的变化后，[Guillaume]和[P1kachu]怀疑该设备甚至能够保存修改所有已知实现所需的信息。听了设备的输出，以及对电路的快速分析，然后打开他们发现的单个芯片，表明他们的怀疑是有道理的。讲座以一个扩展的问答结束，增加了更多关于汽车黑客的信息。那些没有车的人可以拆掉[热熔胶枪](https://hackaday.com/2017/11/23/glue-gun-teardown-reveals-microcontroller-mystery/)、[多普勒模块](https://hackaday.com/2017/09/11/doppler-module-teardown-reveals-the-weird-world-of-microwave-electronics/)或古董[计算器](https://hackaday.com/2017/09/11/doppler-module-teardown-reveals-the-weird-world-of-microwave-electronics/)。

[https://media.ccc.de/v/34c3-8758-how_to_drift_with_any_car/oembed](https://media.ccc.de/v/34c3-8758-how_to_drift_with_any_car/oembed)