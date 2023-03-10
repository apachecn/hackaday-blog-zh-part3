# 动手操作:新的和！XOR 非官方 DEF CON 徽章

> 原文：<https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/>

在短短两周内，我们将涌入拉斯维加斯的赌场参加 DEF CON。到目前为止，我们最喜欢的部分是每年参加 CON 的非官方硬件徽章。那个和！XOR 团队今年推出了一个令人难以置信的产品，我称之为“ [Bender on a Bender](https://hackaday.io/project/19121-andxor-dc25-badge) ”徽章。他们给了我们两个，所以让我们直接进入，看看这个徽章是怎么回事。

[![](img/2c06a5d077177df9534bee2e53bc68cf.png)](https://hackaday.com/wp-content/uploads/2017/07/surface-finish.jpg)

### 珍贵

和去年一样，这种美感简直太壮观了。我知道这么说很可笑，但 PCB 本身看起来比大多数产品的制造质量都要高。黑色阻焊膜是一种完美的哑光表面，裸露的镀金铜层和哑光白色丝网的战略性使用强调了这一点，组件显然经过精心放置，以产生令人赏心悦目的效果。

这不是该队的第一次竞技表演。他们去年制作了他们最初的以狂欢为主题的徽章——如果你错过了，可以看看[我的亲身体验](http://hackaday.com/2016/07/25/hands-on-the-andxor-unofficial-def-con-badge/)——在短短几分钟内卖出了 175 枚，但在 2015 年[也推出了非未来设计](http://hackaday.com/2015/08/10/all-the-unofficial-electronic-badges-of-def-con/)。今年的解决方案是通过 Kickstarter 进行预售，超过[四倍于他们的融资目标](https://www.kickstarter.com/projects/hyr0n/andxor-defcon-25-indie-badge)。支持者已经收到他们的徽章，并在团队的推特频道上展示他们的作品。

### 闪亮的金属

[![](img/92237a8f67ff43bc5c6a638569761ba3.png)](https://hackaday.com/wp-content/uploads/2017/07/gerber-view-is-very-meta.jpg)

Gerber view; very meta

引擎盖下是什么？嗯，没有兜帽，这是一个 PCB 徽章。疯狂的是，这个徽章实际上是一个无线 SoC 模块的附加组件。挂在本德帽子顶端的里加多 BMD-300 驱动着一切。它包括一个北欧 ARM Cortex M4F，令我沮丧的是，它取消了使去年的徽章如此独特的弹簧天线。

今年的另一个升级是显示屏。该徽章已从单色有机发光二极管，取而代之的是彩色液晶显示器。这个屏幕看起来很棒，事实上，当我第一次玩它的时候，我想它可能是一个彩色有机发光二极管(当然价格会使这几乎不可能)。该显示器与 RGB LED 模块和五个按钮(d-pad 和一个操作按钮)一起构成了用户界面。

### 想玩游戏吗？

交互是事情开始变得非常疯狂的地方。查看下面的视频，了解固件的运行情况。令人印象深刻。显然，电路板背面的 SD 卡可以实现可视化，消除片内闪存通常面临的存储空间限制。

有几个简单的游戏你可以玩，但团队做了一些聪明的事情来扩展这个徽章的功能:将 [Chip-8](https://en.wikipedia.org/wiki/CHIP-8) 解释器移植到 Bender。它可以让他们加载几十个经过验证的游戏，而不会浪费他们自己的开发时间。现在，你可以写你自己的游戏/演示/程序，并把它们放在卡片上，让解释器运行。

这很好，但这个徽章的杀手锏肯定是无线交互。

 [https://www.youtube.com/embed/GYqRIXt7Q4E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GYqRIXt7Q4E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



### 僵尸网络

当徽章都在相同的邻近区域时，蓝牙网状网络将形成。当我运行一个徽章并拍摄第二个徽章时，我尝到了这种滋味(好像这是我第一次拆封它)。启动时，一个徽章发现了另一个徽章，并提醒我“欢迎尼克松”——尼克松是另一个徽章的名字。

[![](img/c0a7bc188381aa0f187e7ff511bc56d6.png)](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/package-contents/)

Also in box

[![](img/e0d6602dbdbe790babf1634c5104c21a.png)](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/card-front/)

Instructions: Front

[![](img/8cd20a990d246011605be4d7b60729e1.png)](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/card-back/)

Instructions: Back

有一个“附近”菜单项会告诉你每个徽章的名称以及信号强度读数。其余的功能是隐藏的，因为徽章需要一个激活码，只有在诈骗开始后才可用。但是上面的说明卡对将要发生的事情给出了一个非常清晰的轮廓。

一个定制的应用程序会让你终端进入徽章。从那以后，一切都是为了保卫你的王国，同时试图接管他人的王国。混合一些来自开发者徽章的神模式特性，你就有了一个有趣的配方。

 [![Rigado wireless module](img/03047dad5cfaac8cb0515ff27fb3c142.png "wireless-module")](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/wireless-module/) Rigado wireless module [![Lovely matte black](img/9c70f392773a7fb7a5b92d52681b5470.png "back-of-badge")](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/back-of-badge/) Lovely matte black [![Superb](img/280dbc097f8718e5e3fe1e8d55e5b76e.png "badge-wide-view")](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/badge-wide-view/) Superb [![Check out the traces](img/b0c2fe692b199994bb00e6165248da07.png "trace-on-the-cigarette")](https://hackaday.com/2017/07/12/hands-on-new-andxor-unofficial-def-con-badge/trace-on-the-cigarette/) Check out the traces

所有和所有，产品和！XOR 设法扑灭是壮观的。他们营销机器的硬件设计、固件、交互性，甚至执行力都是一流的。它们甚至装在有品牌的盒子里，在人们需要带它们上路之前有足够的时间这样做，并在用户遭遇黑客攻击时跟进。

这是一个生意，而是一群朋友出于对五金艺术的热爱而做的生意。

* * *

一些和！XOR crew 将于周五加入我们，参加关于 Badgelife 的黑客聊天:我们今年和过去几年看到的所有非官方硬件徽章背后的运动。