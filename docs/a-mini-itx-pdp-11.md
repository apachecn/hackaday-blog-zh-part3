# 迷你 ITX PDP-11

> 原文：<https://hackaday.com/2018/04/26/a-mini-itx-pdp-11/>

PDP-11 可能是历史上最重要的计算机。这是所有小型机之王，一旦你越过 11/20、11/40 和 11/70 的惊人前面板，你会发现 PDP-11 无处不在。希斯基特卖了一个。这是能运行 Unix 的最小的计算机。有作为 DEC 专业人员出售的桌面版本。我被告知 ticket master——美国所有赛事门票销售的整个后端——仍然在 PDP-11 上运行。

PDP-11 有趣的一点是在其开发过程中出现的小型化。随着时间的推移，早期型号的单总线处理器卡被缩小到一个芯片中。这种单芯片 PDP 后来被苏联人克隆，像大多数老式的东欧电子产品一样，它们在易贝都很容易买到。

[![](img/9bc86e077b0f2f32f9078e19c1f55ac6.png)](https://hackaday.com/wp-content/uploads/2018/04/pdpii.png) 为了他的黑客奖参赛作品，【邵氏】[正在把这些芯片中的一个变成一台现代机器](https://hackaday.io/project/67369-pdpii)。PDPii 是一个将 PDP-11 以带有迷你 ITX 主板的开源主板的形式复活的项目。它会改变游戏规则吗？不，不是真的；三十年前你可以买一台台式 PDP-11。不过，这个项目是把你花 10 美元就能买到的新的旧的股票筹码，转变成类似现代系统的东西。最后，Ticketmaster 可以升级了。

这个项目的设计不太符合迷你 ITX 的规格；它基于 [RC2014 背板 Z80 计算机](https://rc2014.co.uk/)，但台式计算机外壳和电源都很便宜，我相信有人知道如何在一个五又四分之一英寸的孔中安装一个八英寸的软盘。

这种迷你 ITX 背板 PDP-11 的主要特点是重新设计了后来的 PDP 中的 Q-bus，使其更小，制造成本更低，并且仍然可以使用所有相关的引脚。通过对巴洛克式 DEC 标准的一些重新配置，[SHAOS]提出了面包板友好的 Q-bus Extended，或 BBQ-Bus+。这个项目的下一步是收集一些 PDP-11 兼容的俄罗斯кр1801вм2 CPU，并在可能是有史以来复制最多的计算机设计的架构上进行展示。

The [HackadayPrize2018](https://hackaday.io/prize) is Sponsored by: [![Microchip](img/20eb9d92b47da4c15177567c02a65727.png)](https://hackaday.io/microchip)  [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey)  [![Supplyframe](img/2d012d9fc9c7873688699aeadb4742d2.png)](https://supplyframe.com/)