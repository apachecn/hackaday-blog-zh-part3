# hacklet 87–Roomba 项目

> 原文：<https://hackaday.com/2015/12/05/hacklet-87-roomba-projects/>

iRobot Roomba 于 2002 年首次推出，被视为一款机器人吸尘器。几乎每个黑客、制造者和工程师都立刻想要一个。然而，Roomba 被证明不仅仅是一个真空；这是任何家庭机器人项目的完美基地。不久以后，Roombas 被黑客攻击，不仅仅用来扫地。iRobot 认识到了这一点，并在后来的型号 Roombas 中添加了一个黑客友好的串行端口。他们甚至发布了一个名为 iRobot Create 的无真空版本。成千上万的项目实际上是在 Roomba 的轮子上运行的。本周的 Hacklet 是关于 Roomba 项目的。

[![roomba1](img/ddf4e575d3b06dd8694d9cf82fe65f24.png)](https://hackaday.io/project/8629) 我们先从【fuzzie360】和[穷人的树莓 Pi Turtlebot](https://hackaday.io/project/8629) 说起。[Fuzzie360]让他们的 Roomba 运行机器人操作系统(ROS)。ROS 实际上是在一个板载的树莓 Pi 上运行的。虽然 Willow Garage 可能会倒闭，但 ROS 仍然是由 Unbounded Robotics 运营的开源项目。安装它可能是一件苦差事。虽然[Fuzzie360]还没有给出完整的教程，但如果你遇到困难，他们会提供建议。

树莓 Pi 对于 Roomba 内置的简单传感器套件来说太过了，但对于微软 Kinect 的[fuzzie 3680]修改设置来说却是完美的。[fuzzie 360]的目标是拥有一个可以用吸尘器清扫大学公寓敌对区域的机器人。

[![roomba2](img/e749fc0e1f54d70bcac0bba3d099ceb9.png)](https://hackaday.io/project/5790) 接下来是【Sircut】，他[升级了他的 Roomba 的电池](https://hackaday.io/project/5790-lithium-battery-upgrade-for-roomba)。早期的 Roombas 设计使用镍金属氢化物(NiMH)电池。单个电池内置于专有的 iRobot 电池组中。然而，镍氢电池无法与锂离子电池相提并论。如今，锂离子电池在手机和笔记本电脑等设备中非常常见。事实上，[Sircut]在这次升级中使用了 18650 尺寸的笔记本电脑电池。[Sircut]还增加了必要的锂离子电池保护电路，以确保这些电池保持良好状态。伏特计提供了电池没有被过度充电的视觉参考。像这样的升级可能会使 Roomba 的运行时间翻倍，但这是有代价的。Roomba 的原始充电坞站不能再使用，因为板载充电电路不是为锂离子电池充电算法设计的。

[![roomba3](img/d5ffb1632c98ee4724c7f420a261cde9.png)](https://hackaday.io/project/8614) 接下来是【马塞尔·瓦拉洛】与[为通勤机器人](https://hackaday.io/project/8614)的大战。IT 部门如何发泄情绪？当然是战斗机器人！不幸的是，[Marcel 的]同事并不都是编程专家。希望未来他们能有一些编程。不过现在，[马塞尔]已经用几乎所有的 Roomba 机器人创建了一个机器人格斗联盟。每个机器人得到一套 3 个气球和 3 个别针。一个气球代表一个生命。一旦你们的生活都完了，你们就死定了！[马塞尔]还创造了一个升级系统，获胜的机器人可以转移到更强的武器，如火焰喷射器。在他的研究中，[Marcel]发现他的 Roomba 中的刷子足够强大，可以在不启用真空的情况下清扫灰尘和碎屑。所以他在更长的战斗时间里禁用了吸尘器。

[![roomba4](img/e0a68c32dd3955e87226ac25d84f56a8.png)](https://hackaday.io/project/8290) 最后我们有【弗雷德里克·马克斯特伦】和 [ESP8266 控制的 Roomba](https://hackaday.io/project/8290) 。[Fredrick]正在黑一个 ESP8266 模块作为这个小机器人的主计算机。当然，8266 意味着它将携带 WiFi，所以这个机器人需要有一个网络接口。[弗雷德里克的]第一个问题是为 ESP8266 供电。Roomba 的电池在 15 伏左右运行，这肯定对 3.3 伏的 ESP8266 不友好。一个开关直流到 DC 转换器准备就绪，而[弗雷德里克]在易贝找到了完美的候选人。8266 将通过当前所有型号的串行接口控制 Roomba。[弗雷德里克]对这个机器人有很大的计划，包括导航和先进的吸尘算法。

如果你想看到更多的 Roomba 项目，请查看我们新的 [Roomba 项目列表](https://hackaday.io/list/8659-roomba-projects)！如果我错过了你的项目，不要害羞，只要[在 Hackaday.io](https://hackaday.io/adam) 上给我留言。这就是本周的 Hacklet。一如既往，下周见。同样的黑客时间，同样的黑客频道，带给你最好的 [Hackaday.io](https://hackaday.io/) ！