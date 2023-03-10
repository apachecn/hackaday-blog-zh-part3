# 超越康威:来自各行各业的细胞自动机

> 原文：<https://hackaday.com/2017/11/01/beyond-conway-cellular-automata-from-all-walks-of-life/>

在每个极客的成长过程中，都有一段时间他们会了解康威的人生游戏。接下来的一个下午，你通常会发现，标准规则集之所以被选中，是因为大多数其他规则并不有趣，而且你的每一个想法都已经被实现了。这一集经常被记为“学习了细胞自动机”(CA)。虽然重要，但生活的游戏不是唯一的，甚至不是第一个。故事开始于 1970 年《生活》杂志出版的几十年前，当时在一个发生了很多科学的地方:那是 1943 年，地点是新墨西哥的洛斯阿拉莫斯，名字是[约翰·冯·诺依曼](https://en.wikipedia.org/wiki/John_von_Neumann)。

## 概述:什么是 CA？

[![](img/ccf924530cce00c6fcab5fb0ecbf811a.png)](https://www.youtube.com/watch?v=8ZviXPlIhj4&list=PLYX-gWUd7Z1xsAg5cEBlxBzv9LL77lM5N&index=2)

A [cyclic CA](https://en.wikipedia.org/wiki/Cyclic_cellular_automaton) making some waves

名称中的“蜂窝”部分来自于这样一个事实，即 CAs 代表一个网格单元，它可以处于许多已定义的状态。网格可以有任意数量的维度，但有了三维，视觉表现开始碍事，超过三维，大多数人的大脑停止工作，所以二维网格是最常见的——偶尔会有一维的惊喜。在大多数情况下，电解槽的状态是离散的，但是存在连续铸造的子集。在 CA 操作期间，网格中每个单元的未来状态是根据一组规则从每个单元状态确定的，这些规则在大多数情况下考虑了相邻单元的状态。

## CA 的历史

第一个 CA 是在 20 世纪 50 年代末由约翰·冯·诺依曼和斯塔尼斯拉夫·乌拉姆实现的，是为了科学而不是娱乐而发明的。它将一定体积的液体建模为相互影响的离散单元的网络。随后，James M. Greenberg 和 Stuart Hastings 开发了一个模型，用三种状态和一组非常简单的规则来模拟可激发介质中的波传播:

1.  当至少一个邻居处于受激状态时，静止小区将改变到受激状态
2.  退出的细胞将进入不应期状态
3.  处于不应期的细胞将进入休眠状态。

[![](img/b3f7f53324bc0777cb585c8a422c4714.png)](https://www.youtube.com/watch?v=DqLwb_5iMLM&list=PLYX-gWUd7Z1xsAg5cEBlxBzv9LL77lM5N&index=1)

The same cyclic CA, this time spiraling out of control

这种算法的一个变种具有连续的不应期状态，可用于在 GPU 上[解决迷宫](https://hackaday.com/2017/10/23/solving-mazes-with-graphics-cards/)。循环模型扩展了这一思想，允许任意数量的状态，并且如果邻居处于下一个更高的状态，则提升每个单元的状态。这里的“循环”部分意味着最高状态被认为是由最低状态继承的。对于某些设置，这类 CA 的行为类似于振荡化学反应，如[别洛乌索夫–扎博廷斯基](https://www.youtube.com/watch?v=PpyKSRo8Iec)反应。

模拟由简单的局部规则控制的或多或少复杂的现象是 CA 的指导原则。即使有了更精确的数值分析方法，CAs 仍然因其简单性和可访问性而大放异彩。

## 生生世世

从简单规则中产生复杂行为的能力很可能是康威的 CA 如此受欢迎的原因。说句公道话，这种受欢迎程度可能把 CAs 从计算机科学的边缘拉到了中心舞台。在《生命》之后，出现了几个新的 CAs，大肆宣传的高潮是[史蒂夫·沃尔夫勒姆]在一本同名的书中宣布发现了一种“新的科学”。

[![](img/da51afa4698bbe622804bdb406be3383.png)](https://www.youtube.com/watch?v=UxuAM8zqPyY&list=PLYX-gWUd7Z1xsAg5cEBlxBzv9LL77lM5N&index=4)

Langton’s ant wreaking havoc on a world of vertical stripes

这些现代 ca 中的一个是 [Langton 的 Ant](https://en.wikipedia.org/wiki/Langton%27s_ant) ，这是一个特例，因为它只查看网格中的单个单元，而忽略了它的邻居。这个细胞被认为是蚂蚁的位置，蚂蚁可能会朝四个主要方向中的一个看。在下面的步骤中，蚂蚁的运动只受两条规则的支配:

1.  如果蚂蚁下面的地板是白色的，昆虫会把它涂成黑色，向右转 90 度，然后向前移动到下一个单元
2.  如果地板是黑色的，在蚂蚁向左转并前进到下一块瓷砖之前，它会变成白色。

人们可能会注意到，这不是蚂蚁行为的精确模型。康威的模拟和细胞繁殖的方式也是如此。好消息是它们从来就不应该存在。与模拟流体相比，这种新型 CA 更适合于理论应用。在蚂蚁的世界里，通过选择地砖的初始状态，人们可以对其运动进行编程。然后，蚂蚁会像计算机一样，将这些输入转换成其他东西。朗顿的蚂蚁在发明十四年后的 2000 年被证明是图灵完备的。通过任意供应细胞，兰顿的蚂蚁可以成为一台通用计算机。

## 这是什么？蚂蚁的 CA？

但是兰顿的蚂蚁不是最小的有用的 CA。所谓的“基本 CAs”是最基本的设计，是一维的，单元只能有两种状态。其中，最引人注目的可能是[规则 110 初级细胞自动机](http://www.wolframalpha.com/input/?i=rule+110)。

基本 CAs 的简单性将可能的规则集的数量限制为 256 种可能的不同实现。这些规则中的大部分彼此等价，要么是镜像，要么是交换了 1 和 0。剔除重复的，我们剩下 88 个不同的基本 ca。数字 110 存在于这 88 种不同的类型中，这是为基本 CA 提出的[编号系统](http://mathworld.wolfram.com/ElementaryCellularAutomaton.html)【史蒂夫·沃尔夫勒姆】的产物。他真的很喜欢这些微型机器，用 Wolfram 语言使用[规则 20](http://www.wolframalpha.com/input/?i=rule+20) 作为伪随机数发生器就是一个证明。

初级元胞自动机最酷的一面是，它们表现出了它们的大表兄们所熟知的各种行为，从减少随机初始条件到几代内的静态输出，再到连续产生混沌模式。

## 应用和含义

运行流体模拟的 CA 是冯诺依曼和乌拉姆实现的第一个 CA，但不是冯诺依曼设计的第一个 CA。他的第一个 CA 是一个名为“通用构造器”的思想实验，一个可以创建任何其他机器的设备，包括给定指令的它自己。在冯·诺依曼于 1943 年加入曼哈顿计划之前，它是在没有计算机的情况下设计的。

这个设计在他死后于 1966 年首次出版。从那时起，直到 1995 年，通用构造函数的一个变体才第一次被实现。据估计，在当代的硬件上，让机器自我复制需要大约两年的时间。今天，运行在有足够内存的台式电脑上的程序可以在几分钟内完成复制。

[![](img/312f814e2ddca5910c1b20a81b83ee5a.png)](https://www.youtube.com/watch?v=Cbgu06jyMy8&index=5&list=PLYX-gWUd7Z1xsAg5cEBlxBzv9LL77lM5N)

[Wireworld](https://en.wikipedia.org/wiki/Wireworld) is a CA that models digital circuits. These are five clocks producing pulses at different rates.

其他自我复制的 CAs 存在，如[兰顿循环](https://en.wikipedia.org/wiki/Langton%27s_loops)和生命被制造成[自我复制](https://www.youtube.com/watch?v=xP5-iIeKXE8)。CA 已经被提议作为公钥加密中的[单向函数](https://en.wikipedia.org/wiki/One-way_function)，这是基于这样一个事实:即使规则是已知的，计算 CA 的前一个状态也几乎是不可能的，而计算随后的状态是微不足道的。如前所述，CA 可以用来产生伪随机数，[某些类型的](https://en.wikipedia.org/wiki/CoDi)人工神经网络可以被认为是 CA。

今天，CAs 再次处于计算的边缘。沃尔夫拉姆和其他人预示的革命并没有发生。虽然已经有了硬件实现，但是其他的计算机架构占据了主导地位。但是随着现代 GPU 以大量相当小的内核并行运行为特征，从而成为 CA 的完美平台，生命可能会找到一种方式。

[编者按:精选图像代表自动机细胞将自己组装成机器人。我们知道这有点夸张，但是乔为我们制作了这个很酷的艺术品，我们正在运作它。总比另一架黑白滑翔机好，对吧？]