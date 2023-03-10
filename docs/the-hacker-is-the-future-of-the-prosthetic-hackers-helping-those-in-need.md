# 黑客是假肢的未来:黑客帮助那些需要帮助的人

> 原文：<https://hackaday.com/2016/06/08/the-hacker-is-the-future-of-the-prosthetic-hackers-helping-those-in-need/>

[![Rush_valley](img/2361647f7881cb5d9c2ddafab63f211f.png)](https://hackaday.com/wp-content/uploads/2016/06/rush_valley.png)

Even the city’s welcome sign is held high by two prosthetic arms.

在《全金属炼金术士》中，有一个叫拉什山谷的城市，它的主要也是唯一的生意是名为 Automail 的高性能假肢。工程师们漫步在拉什山谷的街道上；最好的有自己的商店，就像萨维尔街的高档服装店一样。当然；这一切都是发生在一部有点可笑的日本漫画中的幻想，但当我走过今年的创客博览会时，我开始怀疑这是否是一个可能到来的未来。

假肢的问题在于损伤、体型和解决方法的多样性。如果损伤高一英寸或低一英寸，就会对假肢与肢体的相互作用产生很大影响。如果皮肤受损或神经不再起作用，就需要不同类型的假体。有些假肢是用来替换失去的肢体，有些是用来帮助患病的身体恢复正常功能。许多只是帮助身体康复的临时助手。不幸的是，这意味着通常情况下，大公司只出售人们最可能需要的假肢；更罕见的情况往往没有解决办法。

[![The e-Nable project doesn't mess around. ](img/c95ab868b07ce90882ca008ebe7e2401.png)](https://hackaday.com/wp-content/uploads/2016/06/6nini.png)

The e-Nable project doesn’t mess around.

然而，我们看到黑客们越来越强，不仅致力于解决问题，而且解决问题。我们去年的半决赛选手之一， [openbionics](http://hackaday.com/2015/09/20/hackaday-prize-semifinalist-openbionics-affordable-prosthetic-hands/) ，启发了我们稍后将要讨论的一个项目。还有[机器腿](http://hackaday.com/2016/05/25/hackaday-prize-entry-robotic-prosthetic-leg-is-open-source-and-3d-printable/)。我们在 MRRF 遇到了一个家伙，他一直在为他的儿子做 3D 打印手，他的儿子来自于电子打印项目。

沿着这些思路，我们在今年的 Maker Faire 上看到了两个非常酷的项目:第一个是[电动辅助手套，或 MAG](http://motorassistiveglove.github.io/) 。MAG 旨在帮助周围神经病变患者在漫长的康复过程中重新获得手部功能。[周围神经病](https://en.wikipedia.org/wiki/Peripheral_neuropathy)是一种疾病，通常由糖尿病、毒素暴露或感染引起，其中神经受损，通常手脚不再活动或以有用的方式感觉。一旦疾病全面爆发，以前有能力的人会发现自己无法做简单的事情，如拿一罐汽水或牢牢抓住门把手打开它。

[![The Motor Assistive Glove](img/38d352c923042abc633f0e200c1e62e0.png)](https://hackaday.com/wp-content/uploads/2016/06/themag.jpg)

The Motor Assistive Glove

我们有机会采访了 MAG 团队的成员之一，[Victor Ardulov]，您可以在下面的视频中看到。[Victor]和他的团队在圣克鲁斯大学开始了一个研究项目，开发运动辅助手套。背后的概念很简单。患有周围神经病变的人通常手部有一些运动，但没有力量。MAG 的指尖有一些压力传感器。当用户在垫上施加压力时；手套合上了手指。当压力消失时；手套打开。这个概念很简单，但是通往实用的道路是漫长的。

 [https://www.youtube.com/embed/hWOFtzE1STc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hWOFtzE1STc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



他们克服了手套设计中的许多障碍，其中许多并不明显。例如，如果你想让伸出的手指缩回，弹簧可能是你的首选。然而，螺旋弹簧只关心沿其轴线的位移，如果弯曲，它们提供的阻力要小得多。因此，松紧带被证明是一个更好的解决方案。你是把 3D 打印的部分粘在手套上，还是缝上？为什么引线较长的压力垫会一直失效？这些以及更多的问题都是团队必须回答的。

![motor-assistive-glove-electronics-box](img/3a2dde8e4f9cefa49e26f84a090edb54.png)

A custom motor shield on an arduino.

该设备的大脑是一个位于 Arduino 上的定制电机控制器护罩。虽然 Arduino 有它的缺点，但它仍然一如既往地是易用性的冠军。致动器是小型齿轮有刷电机。看起来像是蜗轮的东西实际上是一根金属线的线轴。当用户按下手指上的衬垫时，电机转动并向下拉电缆，使手指收缩。为了伸展，电机反转并让电缆退出，手指通过手背上的弹性带回到其静止状态。

该小组希望将手套送到另一个项目所在的州；也许像 e-Nable 这样的公司可以帮助那些需要帮助的人。如果你想投稿或查看他们的进展，他们的[网站在这里](http://motorassistiveglove.github.io/)。

[![BentoArm](img/463e25cfc632e00b5777a794cf4615e0.png)
](https://hackaday.com/wp-content/uploads/2016/06/bentoarm.jpg)

更接近汽车的一面，是我们在 Maker Faire 上看到的另一个项目， [Bento-Arm](https://github.com/blincdev/Bento-Arm-Hardware) 。便当手臂是阿尔伯塔大学 BLINC 实验室的一个研究项目。与 MAG 不同，Bento 的手臂距离拿一罐汽水还有很长的路要走；骄傲地附在某人的肩膀上。它的目的是降低那些希望试验先进肌电假体的人的障碍。Bento 臂包括 5 个自由度(肩旋转、肘弯曲、腕旋转、腕弯曲、手张开/合拢)。解剖学上也是正确的。

[!["Like I've been sayin' The future is already here — it's just not very evenly distributed." - William Gibson if he read this article.](img/0a911546b6808aaf8ed02c9c0464fe23.png)](https://hackaday.com/wp-content/uploads/2016/06/william_ford_gibson.jpg)

“Like I’ve been sayin’, the future is already here — it’s just not very evenly distributed.” – [William Gibson](https://en.wikipedia.org/wiki/William_Gibson) if he read this article.

即使你今天可以拥有一个功能完美的手臂:一个可以完美地检测电信号并将其转化为超级平滑、超级强劲的运动的手臂，它充其量也只是有点用处，在更糟糕的情况下，它对用户来说更是一个危险而不是一个好处。

幸运的是，我们生活在一个拥有无人驾驶汽车和五美元单芯片电脑的世界。可以毫不夸张地说，我们已经拥有了一个完美假肢的所有组件；它只需要一点点机器人胶水就能把它们粘在一起。当然，这需要在机器学习、人机交互和所有相关领域进行大量的研究。

便当手臂不是便宜的手臂，但是考虑到一个低端的肌电手臂可能要 5 万多美金……嗯，是便宜的手臂。致动器是现成的 Dynamixel 品牌的伺服系统。这些高端伺服系统备有位置控制、速度和负载传感器，以及一个有用模式的工具箱。想让它们充当减震器？他们能做到。

手臂的框架是 3D 打印的。这一切都是为了使它仍然可以一起去，即使有一个正常的 RepRap 风格的打印机可以满足公差。控制软件已经为 ROS(机器人操作系统)和 MatLab 编写；如果你曾经在机械工程教授身边呆过，你就会知道没有 MatLab 他们会紧张。

[![The Handi Hand does look pretty handy. ](img/b3df3653b456d7bf17b3a79ad3926ed6.png)](https://hackaday.com/wp-content/uploads/2016/06/handy.jpg)

The Handi Hand does look pretty handy.

[![Lovecraftian horror, or just a man with an advanced prothesis?](img/61a4982f4e2a53fffef33c47fd692717.png)](https://hackaday.com/wp-content/uploads/2016/06/pans-labyrinth.jpg)

Lovecraftian horror, or just a man with an advanced prothesis?

当然，和手臂一样酷的是他们的 Handi Hand，定于今年晚些时候开源发布。它连接到便当臂上；之后，整个装配开始看起来非常未来。Handi 手的五个手指都可以运动，可以进行位置反馈，甚至手掌上还有一个摄像头。这让你对潘实验室里的怪物产生了怀疑。

因为它只是一直向下伺服，所以可以用任何输出 0-5V 范围内的 PWM 信号的微控制器来控制手。他们当前的库是为 Arduino Mega 编写的，但这很容易移植。

最终，这个项目组合在一起，形成了一个令人印象深刻的机器学习平台。只需一架顶级的四轴直升机和几个深夜，任何黑客或大学都可以研究下一代机械臂。那很酷。如果你想接触这个项目，这里有[链接。](https://blincdev.ca/)如果你想造一个便当手臂，他们已经在 GitHub 上发布了[的完整设计](https://github.com/blincdev/Bento-Arm-Hardware)；它甚至还有组装手册！

最后归结到这一点。随着家用快速成型技术的进步，世界各地科学家、医生和工程师的持续工作已经将假肢领域不仅带入了黑客手中，还通过他们进入了普通人的生活。很明显，这是一个任何人都可以积极参与并立即开始提供帮助的领域。无论你只是在 e-enable 上注册，在你的打印机闲置的时间里开始打印零件，或者如果你在 Blinc 和 MAG 等人所做的工作基础上更进一步，以制造像天行者家族喜欢在战斗后得到的手一样漂亮的手，这都是一个令人兴奋的黑客时代。