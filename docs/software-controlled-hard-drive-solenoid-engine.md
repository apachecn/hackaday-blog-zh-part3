# 软件控制的硬盘螺线管引擎

> 原文：<https://hackaday.com/2016/01/15/software-controlled-hard-drive-solenoid-engine/>

[杨奇煜-乔托]提交了他的[有趣的螺线管引擎](https://hackaday.io/project/9181-software-controlled-solenoid-engine)。在内燃机、蒸汽机或气动活塞发动机中，动力是由膨胀的气体产生的。在[杨奇煜]的小引擎中，它是由硬盘驱动器臂产生的。螺线管引擎通常只是为了展示，各种形状和大小的[都有。如果你想用电力移动东西，轴向马达可能是一个更好的选择。但是如果你想要一个挑战和学习经历，这是很难击败的。](http://hackaday.com/2015/10/05/radial-solenoid-engine-is-undeniably-cool/)

[杨奇煜]在他的发动机进行第一次革命之前有一些问题要解决。就像活塞发动机一样，正时需要精确。手臂在错误的时间开火会导致各种各样的麻烦，相当于内燃机的逆火。STM32f4 发现板与霍尔效应传感器和 MOSFET 耦合。当电路板得知机械臂已经回到最有效的发射位置时，它通过线圈发出一个脉冲。就像普通发动机一样，正确的正时会带来很大的不同。一旦[杨奇煜]调整好，他的发动机就能以稳定的 3000 转/分的速度运转。

 [https://www.youtube.com/embed/V4Et5AvYgXc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V4Et5AvYgXc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

