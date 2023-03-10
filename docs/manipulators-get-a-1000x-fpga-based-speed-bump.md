# 机械手获得 1000 倍基于 FPGA 的减速带

> 原文：<https://hackaday.com/2016/07/23/manipulators-get-a-1000x-fpga-based-speed-bump/>

对人类来说，移动我们的手臂和手到一个物体上拿起它是相当容易的；但是对于操纵者来说，情况就不同了。一旦我们找到了我们希望机器人捡起的物体，我们仍然需要规划一条从我们的机器人手到物体的路径，同时拖着剩余的肢体前进*而不要让*在任何到来的障碍上绊住它们。所有可能的关节构型的空间称为“关节构型空间”规划一条通过它们的无碰撞路径被称为*路径规划*，这在机器人领域是一个很难快速解决的问题。

如今，机器人专家已经敲定了一些算法，但执行它们需要数百毫秒的计算时间。结果呢？机器人大部分时间都在“思考”移动，而不是执行实际的移动。

一段时间以来，机器人一直步履蹒跚，直到最近杜克大学的研究人员将大部分计算推到 FPGA 上的硬件上。结果呢？[带 6 自由度机械臂的硬件路径规划](http://spectrum.ieee.org/automaton/robotics/robotics-software/custom-processor-speeds-up-robot-motion-planning-by-factor-of-1000)计算时间不到一毫秒！

值得一问:为什么这个问题这么难？硬件是如何让它变得更快的？这里有几层，但值得调查大的。规划从 A 点到 B 点的路径通常是概率性的(随机迭代到终点)，如果存在路径，算法会找到它。然而，当我们需要拖着我们剩余的肢体穿过空间到达那个物体时，问题就出现了。这个特征被称为扫描体积，它是我们的机器人肢体从 A 到 b 时所包围的整个形状。这不仅仅是手的无碰撞路径，而是整个关节集的无碰撞路径。

![swept_volume](img/55008428017b0a81e98349dfc4e4be29.png)

Image Credit: Robot Motion Planning on a Chip

在计算机上对地图进行编码是通过将空间离散成足够分辨率的 3D 体素来完成的。如果一个体素被一个障碍物占据，它会得到一个状态。如果它没有被占用，它会得到另一个。为了计算路径是否可以，需要将代表扫描体的一组体素与代表环境的体素进行比较。这是 FPGA 发挥减速带作用的地方。通过硬件实现，体素占据被编码为比特，并且整个体积计算是并行进行的*。为这个定制硬件很棒，对吧？*

 *我们为杜克大学的人们将它投入运行而鼓掌，我们迫不及待地想看到定制的“机器人路径规划芯片”有朝一日上市。不过现在，如果你想深入了解 FPGAs 如何并行化传统算法，请查看几个月前我们的[线性时间排序功能](http://hackaday.com/2016/01/20/a-linear-time-sorting-algorithm-for-fpgas/)。

 [https://www.youtube.com/embed/u4snHh_S_Ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u4snHh_S_Ao?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

*