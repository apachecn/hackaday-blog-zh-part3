# 麦迪逊集市

> 原文：<https://hackaday.com/2016/05/15/madison-maker-faire/>

周六是首届麦迪逊迷你创客节。在这种情况下，我住在威斯康辛州的麦迪逊市(抱歉，麦迪逊市，SD )。当然，我不是这个领域唯一疯狂的硬件黑客。我一到那里就差点被本·海肯登绊倒，他也住在这个地区。

![ben-heck-gameboy](img/2c6a86e9eb91ab25e32763deb9856b31.png)

看看他展示的那个不可思议的巨型游戏机。好吧，你心里想:树莓派和液晶显示器。不对！他实际上是用 FPGA 来驱动 LCD。更酷的是，它使用了一个原始的 Game Boy brain board，FPGA 连接到它，以便转换手持设备的 LCD 连接器信号，与大 LCD 一起工作。

 [![Plans for a coffee table version](img/3250789d65d697a5df32e6b0352b044b.png "arcade-controller-coffee-table-plan")](https://hackaday.com/2016/05/15/madison-maker-faire/arcade-controller-coffee-table-plan/) Plans for a coffee table version [![Teddy poses with his arcade controller](img/812e8d579098c87aef6e841a8bee23a1.png "arcade-controller-creator-teddy")](https://hackaday.com/2016/05/15/madison-maker-faire/arcade-controller-creator-teddy/) Teddy poses with his arcade controller [![Wires!](img/dc74966ae2831743e8186876118b8825.png "arcade-controller-wiring")](https://hackaday.com/2016/05/15/madison-maker-faire/arcade-controller-wiring/) Wires!

说到游戏，看看泰迪在不到一周的时间里一起黑了什么。这是一款双人桌面街机控制器。在布置好按钮和操纵杆后，他将它们焊接到一个 iPac 控制器上，这使得用户在运行 T2 的树莓派中的动作变得非常简单。他计划扩展这项工作，并向我展示了他的初步计划，准备在咖啡桌上做一个版本。

 [![Aluminum sculpture](img/02a47a081f88a1c381d3b505381f3e08.png "hi-life-sculpture")](https://hackaday.com/2016/05/15/madison-maker-faire/hi-life-sculpture/) Aluminum sculpture [![Intricate laser cut box designs](img/21a11e2335bb7bc050d67ceacc637ec5.png "laser-cut-boxes")](https://hackaday.com/2016/05/15/madison-maker-faire/laser-cut-boxes/) Intricate laser cut box designs [![Sculpture held upside down shows how it's made](img/560df233ffd31cbc746ba3e1d57d168b.png "madison-maker-faire-featured")](https://hackaday.com/2016/05/15/madison-maker-faire/madison-maker-faire-featured/) Sculpture held upside down shows how it’s made

我听说过镇上的博迪吉，一个黑客空间，但还没有时间去参观。很高兴见到一些正在展示来自这个空间的酷作品的成员。对我来说，最有趣的是一件由米勒高寿命易拉罐回收的铝制成的艺术品。你[把熔化的铝倒在水 Balz](https://www.youtube.com/watch?v=KdpQo3tRPLY) (一种吸水的聚合物)上。冷却后，把不是铝的东西都拿走，翻过来。我也喜欢复杂的激光切割胶合板箱。

![line-following-garbage](img/0dc4804a34c2c57bb90f0269faef8f3e.png)

我被这个摊位吸引了，就是你在爸爸和儿子之间看到的那个小机器人。它有一个超大的脑袋达斯·维达(有人戴黑色头盔吗？)这是一个船用电池，带有树莓 Pi、网络摄像头和两个电机。一个 WiFi 加密狗和聪明的网页代码将机器人放在你的手机上，由你随心所欲地驱动。

但主要展示的其实是他们背后的绿色回收容器。你看到的轮子是股票的替代品，由齿轮电机和链条驱动。这是一个循线机器人。在垃圾回收之夜，你按下一个按钮，容器就会沿着车道上的电线自动拖到路边。这是我能得到的(但如果你真的想赢得我的心，你必须制造一个洗衣机器人)。他们发布了一段视频，展示了[回收站与 PiBot](https://www.youtube.com/watch?v=aBrO5Mwi8lg) 完成的相同壮举，但我们希望团队在开始演示半自动版本时[会点击我们的提示热线](http://hackaday.com/submit-a-tip/)！

 [![Ankle and Wrist straps plus the base station](img/0ae326b99637a424837f6ed6e983c928.png "music-in-motion-collage")](https://hackaday.com/2016/05/15/madison-maker-faire/music-in-motion-collage/) Ankle and Wrist straps plus the base station [![They had great signage!](img/63cd6652084b2e3b69b16fd99233acb3.png "music-in-motion-diagram")](https://hackaday.com/2016/05/15/madison-maker-faire/music-in-motion-diagram/) They had great signage! [![Synth built in Pure Data](img/e71ffb6866c4b8ca5fc814e890ef1706.png "music-in-motion-puredata")](https://hackaday.com/2016/05/15/madison-maker-faire/music-in-motion-puredata/) Synth built in Pure Data

麦迪逊迷你创客节的亮点是动态音乐。朴实无华的展台展示了我最喜欢的一项技术:用户增强音乐。自从视频游戏 *SSX 诡计*以来，这在我的灵魂中占据了一个温暖的位置，在这个游戏中，随着你完成更多的滑雪板动作，音轨会变得更好。

这里没有滑雪板，但你确实做了一些可爱的动作。开始时，在每个手腕和脚踝上绑一个 Velcro 带，然后开始跟着节拍移动。每个波段都有一个 Arduino ~~Nano~~ Pro Mini，带有 ADXL335 加速度计和 nRF24L01+无线模块。它们与基站(坐落在乐高乐园中)进行通讯，并被输入电脑。音乐是由[纯数据](https://puredata.info/)驱动的，【卡尔文】用它来创造一个合成器和鼓环，当你完成令人敬畏的动作时，它会变得更加令人敬畏。这是我们这个时代的任天堂电源垫，它…你猜对了…太棒了。

我在 Madison Mini Maker Faire 玩得很开心，迫不及待地想在这个周末去 BAMF。尤其是…呃..我们每年都举办很棒的派对。