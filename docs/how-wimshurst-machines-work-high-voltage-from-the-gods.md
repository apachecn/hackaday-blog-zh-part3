# 威姆斯特机器:来自上帝的高电压

> 原文：<https://hackaday.com/2017/03/03/how-wimshurst-machines-work-high-voltage-from-the-gods/>

[![Wimshurst machine demo](img/ada351b4a4adcbd2e4e99bd78158266b.png)](https://hackaday.com/wp-content/uploads/2017/03/wimshurst_machine_demo.gif)

Wimshurst machine demo

Wimshurst 机器是最古老、最著名的静电机器之一，由标志性的两个反向旋转圆盘和两个莱顿瓶组成。最常见的是，你会看到有人用手摇它，产生火花，尽管我们已经看到它被用得更多，包括为清除烟雾的烟尘净化器提供动力，甚至为激光器提供动力的 T2。

它通过一系列有趣的事件运作。大多数的解释试图把它们都塞进一张图片里，需要一些大的精神体操来想象。这通常意味着人们放弃，听天由命地通过一些人类无法理解的神秘机制来承担这些工作。

所以取而代之，我们来做一个循序渐进的解释。

## 开始:向各个部门收费

![Overview of sectors](img/692ae9c8668dff3f66a1c206acd3d1e1.png)

Overview of sectors

每个磁盘的朝外的一面都覆盖着金属扇区。这一系列事件始于任何带不等量正电荷或负电荷的扇区。只要扇区干净干燥，那么通常至少有一个是充满电的。让我们举个例子，一个带负电荷，在前面的圆盘上。

净负电荷影响后面磁盘上最近的扇区，将负电荷排斥到它的远侧，使近侧带正电荷。这被称为[静电感应](https://en.wikipedia.org/wiki/Electrostatic_induction)，正因为如此，Wimshurst 机器被称为影响机器，因为一个扇区上的电荷会影响另一个扇区上的电荷分布。

接下来，让我们切换到后面的磁盘，看看受影响的扇区发生了什么。

![The neutralizer bars neutralizing](img/6679a42b9be5340006e0f3594363f1e7.png)

The neutralizer bars neutralizing

接下来发生的事情才是真正的天才。每个圆盘都有一个面向它的中和棒。空档器杆的每一端都有一个刷子，当扇面经过时，刷子会接触扇面。并且有偶数个扇区。这意味着当电刷接触到一个扇区时，中和棒将该扇区与中和棒另一端的另一个扇区电连接。这会让它们短路。

假设一个中和刷接触到了受影响的区域，如上图所示，这个区域的电荷被重新分配，使得它的正面向内，而接触到中和刷的一面为负。尽管这个区域总体上是中性的，但中和棒只能看到带负电的一面。现在，它看到了两把刷子接触到的两个部门之间的不平衡。这导致电流流动以恢复平衡。一些负电荷会从我们受影响的部分流向其他部分。从中和棒的角度来看，它现在已经中和了两个区域的电荷。

![Influencing other sectors - rear and front views](img/d15ae5edd74b2d1c34b890404995d90c.png)

Influencing other sectors – rear and front views

当磁盘旋转扇区远离中和棒时，第一个扇区带正电，刚刚带走一些负电荷。并且在接收到该负电荷后，另一个扇区带负电荷。

当这些带电扇区被磁盘正面的中和棒的刷子接触时，这些带电扇区旋转得更厉害。因此，新带电的扇区影响更多扇区的电荷，等等。

一个有益的认识是，这种影响和中和事件导致一个扇区使另一个磁盘上面对它的扇区带相反的电荷。我们带负电的部门创造了带正电的部门。一旦磁盘旋转，带正电的扇区就会产生一个带负电的扇区。

## 对收藏家的指控

![Whirling charges and collectors](img/b773523b5ec6dee4faf26998c4ad8adf.png)

Whirling charges and collectors

前后圆盘(旋转方向相反)产生如上所示的电荷。

这可能需要一段时间来说服你自己(因为你是并排看到前视图和后视图)，但所有带负电的扇区都流向左边的收集器，所有带正电的扇区都流向右边的收集器。您还会注意到，刚刚通过收集器的扇区已经收集了它们的电荷。它们总体上又是中性的，直到它们接触到中和剂刷子，在那里我们上面提到的影响和中和作用使它们重新充电。

 [![Collector with corona](img/f2b57b8ad9e8d51c3d972a7e60de98f1.png "Collector with corona")](https://hackaday.com/2017/03/03/how-wimshurst-machines-work-high-voltage-from-the-gods/wimshurst_collector_with_corona/) Collector with corona [![Collector close-up](img/431d119cac5dd4fa3a39c581e6d76193.png "Collector close-up")](https://hackaday.com/2017/03/03/how-wimshurst-machines-work-high-voltage-from-the-gods/wimshurst_collector_closeup/) Collector close-up

收藏家不会碰这些扇区。相反，它们具有面向扇区的尖点，并且在它们之间具有空气间隙。这是一种我们以前在范德格拉夫发电机的[功能中见过的熟悉技术。每个收集器都有尖角，面向两个磁盘上的扇区，便于传输。](http://hackaday.com/2017/02/16/how-a-van-de-graaff-generator-works/)

以左边的收集器为例，扇区上的负电荷排斥点上的电子，留下正电荷。由于它们是尖点，正电荷被挤在一起，在尖点附近的间隙中产生强电场。强大的电场撕裂空气分子，开始使空气导电的过程，在这些点附近形成蓝色的电晕。正是这种导电空气使扇形区的负电荷穿过间隙到达收集器。这让这些板块再次保持中立。

类似的事情发生在正确的集电极，只是电荷相反。由于这些扇区是正的，这些扇区将从收集器接收电子，使这些扇区再次成为中性的。

但是所有用来中和这些扇区的电荷是从哪里来的呢？这就是电路其余部分发挥作用的地方。

## 莱顿瓶和火花隙

![The Wimshurst machine circuit](img/5b23888947b2eed5080ad3199a1331dd.png)

The Wimshurst machine circuit

电路的其余部分由一个火花隙和两个莱顿瓶组成。两个莱顿瓶只是两个串联的圆柱形电容器。火花隙也可以被认为是一个电容器，尽管它的电介质很容易击穿，与莱顿瓶相比电容较低。火花隙与莱顿瓶并联，两者都与收集器并联。

这意味着集电极通过圆盘相互连接，但也通过莱顿瓶/火花隙电容器相互连接。

从扇区收集的电荷给莱顿瓶和火花隙充电。莱顿瓶被设计成能承受比火花隙更高的电压，所以首先击穿的是火花隙。当它这样做时，就会产生短路。莱顿瓶中所有累积的电荷通过火花隙迅速放电，形成火花，中和莱顿瓶，直到充电过程再次开始。

## 摘要

总之，通过感应，中和棒被骗去给扇区充电。收集者收集电荷并储存在莱顿瓶和火花隙中。当电荷在火花隙上产生足够的电势时，就会产生火花，使莱顿瓶短路，直到再次收集足够的电荷来产生另一个火花。

但是正如我们所说，它们不仅仅可以用来产生火花。我们在 Hackaday 上看到的两个例子是[为烟尘净化器](http://hackaday.com/2014/03/13/cleaning-up-smoke-with-an-electrostatic-precipitator/)供电和[为茶叶激光器](http://hackaday.com/2015/07/08/legit-hack-creates-tea-laser-power-by-mr-wimshurst/)供电。