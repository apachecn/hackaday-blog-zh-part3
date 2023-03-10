# hack let 96–Pi 零竞赛项目第 3 周

> 原文：<https://hackaday.com/2016/02/20/hacklet-96-pi-zero-contest-projects-week-3/>

日历滚动到了 Hackaday 和 Adafruit 建造的房子的第三周:树莓派零竞赛。我们有将近 100 个条目！每个项目都在竞争 10 个树莓派零中的一个，以及三个 100 美元的 Hackaday 商店礼券中的一个。在本周的 Hacklet 上，我们将会看到更多的参赛作品。

[![tizen](img/354460acbc61833fdbbc9d100c612157.png)](https://hackaday.io/project/9649) 【菲尔" RzR" Coval】正试图[将 Tizen 移植到树莓派 Zero](https://hackaday.io/project/9649) 。对于那些不了解内情的人来说， [Tizen](https://www.tizen.org/) 是一款面向一切的开源操作系统。Tizen 被宣传为从可穿戴设备到平板电脑、智能手机到车载娱乐系统的首选操作系统，由 Linux 基金会和 Tizen 协会管理。虽然 Tizen 可以在很多设备上运行，但 Raspberry Pi 和 Pi 2 仍被认为是“正在开发中的产品”。人们很难运行一个预构建的二进制文件。[Phil]正在将源代码移植到有限的 Pi Zero 平台上。到目前为止，他已经运行了基于 Yocto 的构建，并且系统开始启动。不幸的是，Pi 在引导完成之前就崩溃了。我们希望[菲尔]继续努力，让 Tizen 在 Pi Zero 上运行起来！

[![harm](img/6371918c60f446795a31ed6b7b34328b.png)](https://hackaday.io/project/9657) 接下来是【史隆金】带着[课堂音乐教具](https://hackaday.io/project/9657)。《吉他英雄》教会了一代孩子将闪光转化为玩具乐器上的音符。[Shlonkin]正在用类似的想法教学生如何用口琴演奏真正的音乐。Pi Zero 将控制教室前面的大型口琴展示模型。当那个音符被弹奏时，每个孔都会变亮。口琴每个孔有两个音符。[史隆金]用颜色解决了这个问题。红色 led 表示吹气(呼气)，蓝色 led 表示吸气(吸气)。Pi Zero 除了闪烁发光二极管和播放音乐之外还能做很多事情，所以[shlonkin]计划让板子分析学生们演奏的音符。借助一点软件魔力，这个教学工具可以在学生玩耍时提供实时反馈。

[![retro](img/eaa031e1754fedce9efbb9c0fa2257ee.png)](https://hackaday.io/project/9567) 【斯潘塞】正在把圆周率零点当做[【5 美元】自制 Z80 的显卡。](https://hackaday.io/project/9567)这里的 Z80 是 RC2014，他的 DIY 复古电脑。RC2014 是作为 [2014 复古挑战赛](http://www.wickensonline.co.uk/retrochallenge-2012sc/)的一部分建造的。计算机工作时，只有一个 RS-232 串口，用于与外界通信。除非你附近有一台运行终端软件的电脑，否则 RC2014 没什么用。[斯潘塞]正在通过使用圆周率零点作为他的复古战斗站的前端来解决这个问题。Pi 处理 USB 键盘输入，转换为 RC2014 的串行输入，然后通过 HDMI 或复合视频连接显示输出。在 kicad 和 OSHPark 的帮助下，最终的设计通过定制的 PCB[斯潘塞]适合 RC2014 背板。

[![bramble](img/27184e20727c9aaacb49e5a76400408a.png)](https://hackaday.io/project/9576) 终于我们有了【txdo.msk】与 [8 叶丕零荆棘](https://hackaday.io/project/9576)。每台 5 美元，人们争先恐后地使用 Raspberry Pi Zero 构建大规模并行超级计算机。当然，这些不是实用的机器，但它们是学习并行计算基础的好方法。只需要几个连接器就可以让 Pi 零点启动并运行。然而，8 块互连的电路板很快就会让桌子变得凌乱不堪。[Txdo.msk]正在设计一个 3D 打印的模块化盒子来容纳每一片叶子。叶子滑入树莓盒中，防止任何东西短路。[Txdo.msk]已经经历了几次迭代。我们希望他有足够的 PLA 储备来打印他的最终设计！

如果你想看到更多的参赛者参加 Hackaday 和 Adafruit 的圆周率为零竞赛，[请查看提交列表](https://hackaday.io/submissions/adafruitpizerocontest/list)！如果你在那个列表上没有看到你的项目，你不用联系我，[只要提交给圆周率零点大赛](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)！这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！