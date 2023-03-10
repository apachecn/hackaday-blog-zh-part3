# hacklet 73–视差推进器项目

> 原文：<https://hackaday.com/2015/09/04/hacklet-73-parallax-propeller-projects/>

2006 年，Parallax，Inc .对电子行业来说并不新鲜。它们从 1987 年就存在了。尽管如此，对于一家相对较小的公司来说，涉足定制芯片是一大飞跃。Parallax 不仅仅是跳到一些千篇一律的 ASIC，他们还制作了自己的并行多核微控制器。由[Chip Gracey]设计的视差推进器有 8 个核心，称为齿轮。Cogs 通过集线器连接到 I/O 引脚和其他资源。该推进器取得了商业上的成功，并继续拥有忠实的追随者。本周的 Hacklet 是关于 [Hackaday.io](https://hackaday.io) 上一些最好的推进器项目！

[![woz](img/9577ffd8ce0ac33713f1754a18d21fb6.png)](https://hackaday.io/project/3620) 我们先从反推 prop Star【Jac gouds MIT】和[L-Star:Minimal Propeller/6502 计算机](https://hackaday.io/project/3620)开始。[Jac]喜欢经典的 6502 处理器。受到[本·黑肯登]最近制作的 Apple I 的启发，[Jac]想看看他能否用最少的零件复制一个 Apple I。他在他的[软件定义的 6502 计算机](https://hackaday.io/project/1283)项目成功的基础上，创建了 L-Star。整个东西可以放在一个有多余空间的螺旋桨原型板上。该项目使用 6502，螺旋桨处理几乎所有其他事情。该系统从 PS-2 键盘输入，并通过复合视频输出，就像最初的 Apple I 一样。正如你从照片中看到的，它非常能够以 ASCII 显示 Woz。[Jac]已经扩展了 L-Star 以支持俄亥俄科学 C1P 和 CompuKit UK101，这两个都是早期基于 6502 的计算机。

[![bbot](img/d0a6310991429d0b83b51d0cff6bced4.png)](https://hackaday.io/project/4652) 接下来是【迈克 H】和 [B-BOT](https://hackaday.io/project/4652) 。B-BOT 是一个平衡机器人。[Mike]使用 B-BOT 来学习螺旋桨设计和 SPIN 编程，SPIN 是螺旋桨的内置解释语言。虽然比汇编程序慢，但 SPIN 的速度足以解决经典的倒立摆问题。B-BOT 的主要传感器是 Pololu AltIMU-10。这个模块包含一个陀螺仪，加速度计，指南针，高度计都在一个小板子上。运动以两个步进电机的形式出现。指挥和控制是通过 X-Bee 无线电模块。所有的零件都装在一个定制的 PCB 上[Mike]用他的 CNC 路由器铣出来的。

[![xynq](img/70b6efdae1b8e5d77f681f44a60363b4.png)](https://hackaday.io/project/6786)【antti . lukats】创造了[软推进器](https://hackaday.io/project/6786)，他的参赛作品在 2015 年 Hackaday 奖。软推进器根本不用硬件推进器。该系统的核心是 Xilinx Zynq-7 芯片，它包含一个 FPGA 和一个双核 ARM A9+处理器。回到 2014 年，Parallax 发布了螺旋桨核心的 Verilog HDL 代码。[Antti]将这些代码移植到了 Zynq-7 上。256Kb 的内存，16 MB 的闪存和一个 LED，整个系统装在一个比口香糖还小的 DIP 封装中。

[![pipman](img/c83dbb40427536de11c0b6b5e1e0217e.png)](https://hackaday.io/project/2503) 最后，我们有【克里斯蒂安】与[皮普曼 GPS 手表](https://hackaday.io/project/2503)。只是有些关于辐射系列游戏中的小男孩。这种个人信息处理器(PIP)已经产生了数百个来自角色扮演者和电子爱好者的项目。[克里斯蒂安的]版本使用 4D 系统公司的 TFT LCD 来显示这些令人惊叹的图形。输入来自一个 5 向导航开关。GPS 和指南针模块提供了 Pipman 需要的所有导航数据。在它的中心是一个旋转编程的视差推进器。[克里斯蒂安]在他的工作台上有一个工作原型。他现在正在用 Blender 制作一个 3D 打印的盒子。

Hackaday.io 上有一大堆螺旋桨项目，如果你想看更多，可以查看我们的[螺旋桨项目列表](https://hackaday.io/list/7549-parallax-propeller-projects)！我错过你的项目了吗？不要害羞，[在 Hackaday.io 上给我留言就行了](https://hackaday.io/adam)。这就是本周的 Hacklet，一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 Hackaday.io！