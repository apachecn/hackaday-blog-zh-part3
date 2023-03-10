# 每个人都需要一台个人超级计算机

> 原文：<https://hackaday.com/2018/03/21/everyone-needs-a-personal-supercomputer/>

当你想到超级计算机时，大盒子和闪光灯充满服务器机房的景象立即出现。大约从 90 年代开始，这些超级计算机就成了计算机集群，一起处理一个问题。在过去的二十年里，人们一直在自己家里建造自己的“超级计算机”,现在我们有了廉价的 ARM 单板计算机可以玩。这是什么意思？个人超级计算机。这就是[Jason Gullickson] [为参加 Hackaday 奖](https://hackaday.io/project/85392-rain-mark-ii-personal-supercomputer)而建造的。

[Jason]项目的目标不是进入 500 强，而且它是否会比一个足够现代的桌面工作站更强大也是值得怀疑的。这个项目的目标是给任何人一个与大规模集群具有相同架构的系统，以便于学习高性能应用程序。它还有一个覆盖着 led 的前面板。

该系统的设计是围绕一个 64 位 SOPINE 模块(T1)构建的，或者说，基本上是一个 64 位四核 CPU，贴在一个适合 SODIMM 插座的板上。如果这听起来像树莓派电脑模块，你会得到一块饼干。与 Pi 计算模块不同，SOPINE 背后的人创造了一种叫做“集群板”的东西，即八个*垂直* SODIMM 插座，用一个控制器、电源和一个以太网插孔连接在一起。是的，这是一个用于集群计算的主板。

对此，[Jason]在标准的现成分线板上添加了自己的想法。这个仪表板安装在一个漂亮的铝制外壳上，前面板装有一大堆看起来像古董的红色发光二极管。这些 led 指示集群中每个位的当前负载，提供关于这些计算进行情况的即时视觉反馈。有了正确的艺术——也许是金色、棕色和鳄梨色——这台超级计算机看起来就像是从漂亮的计算机时代走出来的。无论如何，这是 Hackaday 奖的一个很好的参赛作品。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)