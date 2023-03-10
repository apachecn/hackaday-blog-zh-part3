# 重复利用洗衣机中的电机

> 原文：<https://hackaday.com/2017/12/20/reusing-motors-from-washing-machines/>

当你需要完成一项大的工作时，大型汽车是很棒的，但是它们可能很贵或者很难找到新的来源。然而，对大多数人来说，在家里就有一个巨大、肥胖、多汁的发动机来源——花园式洗衣机。这些马达通常需要一个特殊的控制器，然而[【Jerry】在这里向我们展示如何破解机器自带的控制器。](https://hackaday.io/project/28630-variable-speed-washer-motor-and-controller-reuse)

黑客开始于[Jerry]决定挖出一台美泰克 MAH7500 Neptune 正面装载机。许多项目借用电机，但依靠单独的变频驱动器，所以目标是看看机器的原始控制器是否可用。机器首先使用工厂维修模式进行故障诊断，如果一切正常，该模式会以设定的速度旋转滚筒。

从那里，这是一个相对简单的工作来源的机器原理图，以确定各种连接器的引脚。在用示波器和函数发生器做了一些实验后，[Jerry]能够让原控制器做艰苦的工作，让马达旋转起来。

这是一个简单的技巧，并且依赖于文档的可用性来完成工作，但是对于其他任何希望在自己的项目中驱动类似电机的人来说，这是一个很好的灵感。好处是，通过使用原来的电机控制器，你可以相信它是正确的电机额定手头。

也许不是感应电机，你宁愿驱动高功率无刷 DC 电机？这个项目可以提供帮助。