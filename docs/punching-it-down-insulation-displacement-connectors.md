# 向下冲压:绝缘位移连接器

> 原文：<https://hackaday.com/2017/03/07/punching-it-down-insulation-displacement-connectors/>

在我虚度的青春里，我发现自己在一家当地医院做临床实习。我和我的同学们是医院等级制度中最底层的人，承担着科室里的大部分工作，并为这样的特权付出了代价。因此，我们的储物柜设施有点不合格:一个贴着“通信”标签的门后面的壁橱角落。

房间里有一把破椅子，墙上有几个挂衣服的挂钩，还有一个(对我来说)很有趣的配电板。它有一系列的长方形积木，上面有突出的钉子。每块积木都有一根粗电缆，电缆的左边有许多成扇形散开的彩色细电线，它们整齐地连接在一起，右边有一个由蓝色和白色电线组成的老鼠窝。我们被告知不要碰板子。尽管如此，我还是碰了它。

后来我才知道，这些是 66 型接线板，用于该部门的电话系统，在我的黑客生涯中，我使用了相当多的接线板。几十年来，冲压连接器是私有和公共电信物理设备的主要部分，属于一种称为*绝缘位移连接*或 IDC 的电气连接。我们最近研究了[压接如何工作](http://hackaday.com/2017/02/09/good-in-a-pinch-the-physics-of-crimped-connections/)，以及[焊点内部到底发生了什么](http://hackaday.com/2017/02/23/what-the-flux-how-does-solder-work-anyway/)。我想，用一点关于 IDC 的工作方式来补充一下可能会更好。

### 对(更)快速度的需求

由于压接连接是电气和电子行业通过消除焊接连接的劳动密集型步骤来提高组装效率的一种尝试，所以绝缘位移也被开发出来以节省相对于压接的时间。尽管压接连接比手工焊接接头效率高，但在大多数情况下，压接仍然需要大量的手工劳动。即使在装配过程复杂到足以保证自动压接的情况下，完成压接仍需要多个步骤——剥去绝缘层、将电线插入压接连接器，以及施加压接压力，可能需要多次。IDC 消除了导线准备步骤，通过更少的工具更换实现了更快的连接，并且更适合导体的批量端接。

 [https://www.youtube.com/embed/Xl1j4PxKdjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Xl1j4PxKdjE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



IDC 的第一项美国专利于 1961 年颁发给了为明尼苏达矿业和制造公司工作的两位发明家。3M 公司直到现在仍然热衷于 IDC 连接器；我们当中很少有人在汽车上安装过收音机或遥控启动器，他们不会不熟悉 Scotchlock 连接器，这种连接器可以用来接入汽车的线路。原始专利插图显示了与我们今天仍在使用的 Scotchlocks 惊人的相似性，并揭示了所有 IDC 背后的基本思想。一个开槽的金属刀片构成了 IDC 的核心，其槽的大小刚好低于要连接的电线的直径。

### 在插槽中

![](img/39f18a5075ea4d1d3c9b2408ffa46df1.png)

US Patent [3,012,219](https://www.google.com/patents/US3012219)

当绝缘线放入槽中并施加适当的向下压力时，槽切入并移开塑料绝缘，露出里面的导体。随着终端压力的增加，导线接触槽的侧面并开始变形；在很大程度上，压接连接内部的电线股开始流动和拉伸，槽中的电线也有效地冷焊到金属触点，形成气密连接。并且像在压接连接中一样，由增加的压力引起的变形起到松动和驱除会干扰清洁连接的表面氧化的作用。

当然这是一个一般化的情况；每个 IDC 的详细信息都与他们将要从事的工作有关。一些接触槽是锥形的，一些是直的；在一种应用中可能需要槽中的锋利刀片，而钝刀片在其他应用中工作得更好；一些插槽装有弹簧，而另一些没有。用于端接这些连接器的方法也千差万别。仪表板下的简单压锁可能只需要一把钳子，而大量端接 ATA 连接器带状电缆的工具将是更复杂的压力机，可以将力均匀地分布在一长组触点上。

 [https://www.youtube.com/embed/T88PVLUqRJE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T88PVLUqRJE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



在电信领域，昔日的更衣室中的 66 个数据块将使用 66 位类型的手持式打孔工具进行端接。冲压工具本身是一种弹簧加载的冲击工具；当硬化钢钻头放置在触点上，导线装载在槽中时，向下的压力开始将导线推入触点槽中，并克服弹簧压力将钻头推回到工具主体中。当施加适当的压力时，弹簧触发锤子撞击砧座，驱动钻头向下，以恰到好处的压力完成连接。66 型钻头的一侧有一个锋利的刀片，可以在冲压时修剪多余的电线，或者钝头钻头可以用于菊花链连接。

如今，IDC 无处不在——汽车线束，可能是你家里的每一个电器，以及大多数计算机内部的几十个。尽管 IDC 一度被严格限制用于低压连接，但很有可能你会看到 IDC 越来越多地用于[住宅和商业主接线](http://updates.clipsal.com/ClipsalOnline/Files/Brochures/A0000102.pdf)。无需多种工具和手动操作就能实现快速、牢固、气密的电气连接，这种优势太诱人了，不容错过。

[标题图片:By Z22(自己的作品)[ [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0) ， [via Wikimedia Commons](https://commons.wikimedia.org/wiki/File%3A6-Clip_66_Block_B_Series.jpg)