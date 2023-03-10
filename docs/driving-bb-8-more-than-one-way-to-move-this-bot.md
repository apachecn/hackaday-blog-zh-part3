# 驾驶 BB-8:移动这个机器人的方法不止一种

> 原文：<https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/>

BB-8 是 2016 年电影《星球大战:原力觉醒》中推出的备受喜爱的新机器人，尽管在 2014 年发布的第一部预告片中，我喜欢它，因为它提出了有趣的工程问题。你如何制造一个机器人，它是一个滚动的球，但是当球在它下面滚动时，它的头在上面？

 [![BB-8 in 1st Star Wars: The Force Awakens trailer](img/6d1ff2a4a2da11b55bf1b9f46c087624.png "BB-8 in 1st Star Wars: The Force Awakens trailer")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb-8_1st_trailer/) BB-8 in 1st Star Wars: The Force Awakens trailer [![Hamster in hamster wheel](img/34b50ec1f6264c0457f248e539479221.png "Hamster in hamster wheel")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/hamster_in_hamster_wheel/) Hamster in hamster wheel

为了让球滚动，大多数人一开始发现的显而易见的答案是使用仓鼠轮子的类比。跑进去的仓鼠让轮子转动。在相当大的 BB-8 建筑世界中，驱动机制已经被称为仓鼠驱动，或者仅仅是仓鼠。

![Magnets holding the head on](img/f115ed8e087bf7671eadbcb880154659.png)

Magnets holding the head on

对于头部来说，球内显然会有磁铁，也许是通过从仓鼠身上伸出的一根柱子固定在球的顶部附近。相应的吸引磁铁将被连接到头部的下面，球(也安装在头部下面)将保持头部在球上平稳移动。

我所见过的所有 BB-8 建造者都是用磁铁来做头部。然而，仓鼠只是多种解决方案中的一种。自从最初的首次亮相以来，许多不同的方法已经在构建中使用，我们将会很高兴地看到每一种独立的方法。这几乎就像揭示一个魔术；但实际上这都是聪明的工程。

请注意，对于实际的电影，使用了 7 或 8 个道具和 CGI 的组合。在各种宣传活动中展示的正式工作的 b b-8 是在电影制作完成后建造的，截至本文撰写时，他们的建造细节已经公布。然而，一个值得注意的细节是[他们没有使用仓鼠驱动器](http://www.popsci.com/qa-how-to-create-robot-icon)。

以下是我迄今为止见过的所有不同的 BB-8 驱动系统的细节，以及它们是如何工作的。

## 车轴驱动又名钟摆驱动

对于轴传动，轴在球内水平运行，穿过中间的一半。在轴的一端或两端是一个马达，球连接到马达的轴上。

 [![BB-8 axle type cutaway showing the axle, motors and the large mass](img/001dd7c4e4dbbdb5eac4250339e08092.png "Axle type parts")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_axle_type_motors_an/) Axle type parts [![BB-8 axle type cutaway showing the axle, motors and the large mass](img/bc05f7c5474c4970fda1fdc3665b6c21.png "Axle type parts close up")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_axle_type_motors_zoomed_an/) Axle type parts close up

一个大质量悬挂在车轴中间，并固定在车轴上。当马达转动滚球时，滚球会如预期般旋转。大质量沿着球运动的方向向前摆动。但是你可能已经预料到质量会向后摆动。

 [![BB-8 axle type side view cutaway - stationary](img/4ab9be8d544c1084b8dee84191e7839e.png "Axle type side view - stationary")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_axle_type_side_view_stationary_an/) Axle type side view – stationary [![BB-8 axle type side view cutaway - moving](img/4106aa981b732c9ae7eb7830453ac231.png "Axle type side view - moving")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_axle_type_side_view_moving_pend_tilted_an-2/) Axle type side view – moving

如果你曾经拿着一个马达转动一个很大的物体或者很难转动的物体，那么你会回忆起马达想要反方向转动。这很危险，所以不要真的去做，但是想象一下，当你在一块木头上钻孔的时候，你把马达锁在开的位置，然后放开钻头。如果木头被夹住，而且孔足够紧，结果是钻头会反方向旋转。这里也是如此。电机和质量块的旋转方向与球的旋转方向相反。

![BB-8 axle type cutaway showing shifted center of mass](img/95b1b90680c1c72dc7187aa64846dae9.png)

Axle type showing shifted center of mass

另一种可能更正确的方式是，当你向前摆动物体时，重心向前移动，球向那个方向旋转。正是因为这个原因[它也被称为摆动驱动(PDF)(第 2.2.4 节)](http://www.mdpi.com/2218-6581/1/1/3/pdf)。钟摆向前摆动，球朝那个方向旋转。

![BB-8 axle type cutaway showing it turning by tilting the pendulum](img/a68c6e2d16bea5bef5f2ae08d4e0ab03.png)

Axle type turning

假如我的物理学是正确的，摆的质量越大，摆向前摆动的幅度就越小。这在加速过程中也发生得更多。

车轴上的马达不转动。为了转动球，一个质量悬挂在轴的中心。上面提到的摆锤可以达到这个目的。然后，一个马达使这个物体沿着轮轴向任一方向摆动。

将质量摆向一边会使球向那一边倾斜，然后球向那一边移动。仔细看上面的插图，你会发现轴和球实际上是倾斜的，而钟摆由于质量较大而保持水平。这种转身技术意味着球不能在原地旋转，而是必须向前或向后移动(尽管向后和向前在 BB-8 中失去了意义，因为头部可以指向任何方向。)

![Ed Zaricks BB-8 during testing](img/a969ee14430621b5225540edfaf10d5c.png)

Ed Zaricks BB-8 during testing

向前和向后的摆动可以通过再次使用由轴马达驱动的摆锤质量以摆动的相反方向摆动摆锤来最小化。为此，IMU(惯性测量单元)连接在设备上的某个位置。IMU 是电路板上的一个芯片，它知道自己相对于地球的方向(例如 Adafruit 的 [BNO055 分线板)。类似 Arduino 的东西从 IMU 获取信息，并使用它来打开和关闭电机，以移动钟摆并逐渐消除摆动。实现这一点的源代码称为 PID 循环(比例积分微分)。](https://www.adafruit.com/products/2472)

类似地，侧向摆动可以通过在相反方向上侧向摆动质量来处理，尽管我还没有在任何成品轴驱动 b b-8 中看到这样做。要么是没有处理好，要么是下面有足够多的质量，而上面的质量相对较少，使得问题太小而不被注意到。

到目前为止，我已经在网上看到了三个完整的轴驱动 BB-8，照片中显示的是[Ed Zarick]的一个优秀的制作细节。

## 仓鼠驱动器

仓鼠通常是坐在球内的双轮车，不以任何方式与球物理连接。进一步的支持通常是由脚轮或自由旋转的球前后伸出来接触球，帮助保持双轮仓鼠的稳定。移动是通过向同一个方向转动两个轮子来完成的。

 [![BB-8 hamster type cutaway showing wheels, motors and casters and how it moves](img/290dfbf6bbac6138230ac30228c9be6b.png "Hamster type overview")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_hamster_type_intro/) Hamster type overview [![BB-8 hamster type cutaway showing how it turn by rotating the wheels in opposite directions](img/83ccd16eebba992a5d308500af8b334d.png "Hamster type turning")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_hamster_type_turning/) Hamster type turning![Wayne Neumaier's BB-8 during testing](img/0804e10e6242eaf25c7f569e8bcdb65b.png)

Wayne Neumaier’s BB-8 during testing

转向是通过向相反的方向转动轮子来完成的。这意味着每个车轮都有自己的马达。这被称为差速驱动或坦克驱动，因为这就是双履带坦克的转向方式。

一些人通过使用 IMU 来检测摆动，并在 PID 环路中向前和向后驱动电机，从而稳定来回摆动。仓鼠的底部没有太多的空间来放置一个钟摆式的物体，它可以摆动来保持稳定。然而，质量越固定越低，它就越稳定。

你可以看到[【Wayne neu Maier】的仓鼠驱动 BB-8](https://www.youtube.com/watch?v=y4pOeCA7-F4) 在涂球前的最后测试中，如图所示。他的两个轮子在底部附近。

## 无轮毂车轮驱动

无轮毂车轮与仓鼠驱动相似，因为内部有一个独立于球的车辆。这个设计最著名的是[詹姆斯·布鲁顿]为他的 BB-8 版本 3 所做的设计。与仓鼠不同的是，没有轮毂的轮子，所谓的内部车辆被限制在一个轨道上，这个轨道是球的一部分。在下面的插图中，球的侧面没有显示出来，尽管它们通常是附着在轨道上的。这条赛道被称为无轮毂车轮，因为它的中心没有轮毂。

![BB-8 hubless type cutaway showing the hubless wheel, vehicle and location of the drive motor](img/4e672d6f62de60c93dd1c1b4b7a523f3.png)

Hubless type parts

有一个驱动轮是车辆的一部分，它压在无轮毂车轮上并使其旋转(见插图)。它的作用和仓鼠的轮子一样，只是在这种情况下只有一个轮子。车辆受到无轮毂车轮两侧周围的脊的约束。

这种设计的原因之一是球的无轮毂部分可以制造成没有接缝。

对于一个普通的球，球的两个半球在一起有一条缝，这会干扰车内的平稳运行。对于无轮毂车轮驱动，球的中心光环(车辆行驶的路径)可以作为一个整体制造。车辆行驶的内表面是光滑的。当然，当地球的其余部分被添加时，会有接缝，但它们不会影响内部无轮毂车轮车辆的运行。

与其他设计相比，这种设计的优势还在于球的两侧可以像电影中的 BB-8 一样打开访问面板，即使电影使用了道具和 CGI 来做到这一点。

![BB-8 hubless type cutaway showing how it turns by tilting the suspended large mass](img/4e1af58a527d851bc553859562110487.png)

Hubless type turning

转向是以与车轴驱动相同的方式完成的。这辆车有一个像钟摆一样下垂的部分，可以向两边摆动。此处所示的摆锤质量是一个沉重的飞轮(红色)。然后，马达可以将质量摆向任一侧，使球倾斜。就像轮轴驱动一样，倾斜球会导致整个机器人向倾斜的方向移动。

使用类似于轮轴和仓鼠驱动的技术组合来实现稳定。为了前后稳定性，车辆在轨道上前后移动，以对抗摇晃。为了实现左右摇摆的稳定性，悬浮质量会左右摇摆以抵消这种摇摆。

巨大的飞轮也可以绕着自己的轴快速旋转，这使得 BB-8 的其余部分向相反的方向旋转，使其增加了就地转动的技巧。

 [![BB-8's hubless type cutaway showing how it turns on the spot by rotating the flywheel](img/eabb6d8ae4e0c9d582f55982c3de28c2.png "Hubless type flywheel - turning on the spot")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/bb8_hubless_type_flywheel/) Hubless type flywheel – turning on the spot [![James Bruton's BB-8 during testing](img/8b47d93893b0620124bf7cccc1e243f7.png "James Bruton's BB-8 during testing")](https://hackaday.com/2016/06/24/driving-bb-8-more-than-one-way-to-move-this-bot/james_brutons_bb8/) James Bruton’s BB-8 during testing

在上面的照片中，你可以看到[【詹姆斯·布鲁顿的】无轮毂车轮 BB-8 版本 3](https://www.youtube.com/watch?v=ALwVhb-tOcs) 在做所有化妆品之前的最后测试。

## 全轮驱动

![An omniwheel robot (not BB-8)](img/ade80ae72ae3a9c95267bb0527f3414a.png)

An omniwheel robot (not BB-8)

[全向轮驱动](http://hackaday.com/2013/06/08/omniwheel-robot-build-uses-a-bit-of-everything/)类似于仓鼠驱动，车辆在球内行驶，但不同之处在于车辆可以向任何方向移动。这是通过三个或四个全方位轮来完成的，每个轮子都有自己的马达，并朝向自己的方向。

我可能已经错过了，但我还没有看到任何完整的全轮驱动 BB-8 建设。我见过一个 omni wheel drive(就像照片中显示的那个),它驱动一个球，但是还没有头。我还见过一个 BB-8 的工作头使用了 omni 轮，但据我所知，它们只是作为仓鼠驱动轮使用的，尽管我可能错过了使用 omni 轮带来的一些微妙的差异。

## 其他？

它们就在那里，对我来说，知道了让 BB-8 活起来的许多方法，让机器人建造自己变得更加神奇。如果我错过了一些，我不会感到惊讶，事实上我会很高兴。让我们知道你遇到的任何其他人。这些都是非常复杂的系统，我也很想听听你对每个微妙之处的看法。请在下面的评论中留下这些评论和任何其他 BB-8 想法。