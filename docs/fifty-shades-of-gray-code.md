# 五十度灰代码

> 原文：<https://hackaday.com/2017/01/25/fifty-shades-of-gray-code/>

几年前，一家博物馆请我帮助他们完成一个承包商为他们建造的展览。这是一个类似于命运之轮的轮子，但是更小，安装在墙上而不是地板上。你可以转动滚轮，它会停在某个物品上，电脑会播放一段关于该物品的短片。从物理和机械角度来看，这是一个建造精美的展览。然而，电子设备仍有不足之处。

原则上，这是相当简单的计算机任务。测量轮子的位置，当它停止移动时，根据位置播放视频。问题是创造艺术机械的人没有认真考虑它背后的电子设备。有时——但不是经常——转盘会播放错误的视频。有时它根本不播放。

## 头号嫌疑犯

我当时的怀疑证明是正确的。我把轮子从支架上取下，发现背面有铜箔带。每个饼状楔形物的不同区域都有箔片，每个区域都有两把刷子。当车轮停止时，两个电刷会短路在一起，其余的是开路的。他们检测的方式很奇怪，但这不是问题所在。(它涉及一个拆下来的 PS/2 键盘。)

[![ring](img/bedc4e45df33035d8433a031da0ff2ba.png)](https://hackaday.com/wp-content/uploads/2017/01/ring-e1484170884588.png) 有相当多的饼状楔形物，因此该设备的每个楔形物有多个箔条，形成一个 4 位二进制数。也就是说，每个楔形编码一个从 1 到 12 的数字，用箔的存在来表示 1，用箔的不存在来表示 0。例如，下图显示了一个类似的有三个钻头的轮子。从顶部顺时针方向移动，外部轨道上的黑色标记代表形成数字 001 的箔片。然后箔片形成 010，011，最后是 100，覆盖了大部分车轮。

有两个问题。首先，如果砂轮几乎正好在两个区域的中间，两组电刷有可能接触，即使只有一组电刷接触。画笔靠得很近，没有完全固定，箔片也没有非常精确地对齐。在上面的示例轮子上，如果你在顶部，你可能会看到画笔读数为 101，这在这个简单的轮子上甚至不是合法的组合。

另一个小故障发生在箔片在电刷对的一半而不是另一半上的时候。这通常意味着另一个刷子也是半激活的。一条赛道上的刷子越接近，这种可能性就越小，但总有一些可能性，车轮会刚好错误地停止。

## 答案

我对设备做了一些改动。首先，我改变了铝箔胶带绘画，并使用了红外发射器和探测器对。我不认为画笔是可靠的。但是仅仅这样并不能解决问题。整个系统基本上是一个大的自制旋转位置编码器。真正的旋转位置编码器使用格雷码来防止轻微的不对准和边界情况成为问题。对一些人来说，格雷码这个术语(以发明者弗兰克·格雷的名字命名)不够新奇。所以他们称之为二进制反射码。帮你自己一个忙，称之为格雷码。你不会想成为我的老教授，他说“最大化布尔变量”时，他的意思是“设置位为 1。”

不像 ASCII 码，没有一个格雷码。该术语指的是任何二进制数序列，其中每一项与其相邻项之间只有一位差异。在学术术语中，每一项之间的海明距离是 1。

## 汉娩距

最初的车轮使用顺序编码:

```
0000
0001 
0010
0011
...
```

前两个项目之间的汉明距离是 1，但接下来的两个项目的汉明距离是 2，因为您必须翻转两位才能从一个项目进入下一个项目。所以这不是格雷码。不要忘记，当序列循环时，最后一个条目和第一个条目也是相邻的。

考虑具有 4 项的 3 位代码:

```
000
001
011
111
```

这不是格雷码，因为最后一个项目(111)和第一个项目(000)之间的距离是 3。一种可能的正确格雷码是:

```
000
001
101
100
```

当然，代码不必以 000 开头，因此同样有效的代码是:

```
110
010
011
111
```

## 常识

因为每个相邻的项目只有一位不同，所以边缘案例更适合使用物理项目，如笔刷或光学传感器。假设轮盘上有两个饼图楔形区，C 和 D。如果 C 是 011，D 是 100(非格雷码)，那么在边缘有可能得到 111，这可能是其他项目。但是如果 C 是 011，D 是 111(就像上一个例子)，从 C 移到 D 会在某个时候干净地切换到 D。在从 C 到 d 的过程中，不会有任何时候其他代码是可能的。

[![](img/dc1dd7f9912fe2a4832f0b41c5f94890.png)](https://hackaday.com/wp-content/uploads/2017/01/encoder_had_colors.png) 如果你仔细观察一个旋转编码器圆盘，你可以看到图案。轮子有八个饼形切片。如果你考虑三个同心环，你会注意到在每个切片上，一个环不是白色就是黑色，从相邻的切片看，只有一个环是不同的。该图清楚地说明了为什么列表中的第一项和最后一项在逻辑上是相邻的。由于每个邻居只有一位不同，所以磁盘是顺时针旋转还是逆时针旋转并不重要。

## 为什么是灰色？为什么反映？

[弗兰克·格雷]在贝尔实验室设计了这种编码方案，专利可追溯到 1947 年——最初的电路使用真空管和阴极射线管。他没有称之为格雷码，但其他专利称之为格雷码，这个名字就沿用下来了。反映的名称来自一种构造格雷码的方法，在原专利中出现[。后来，格雷因与[赫柏·艾夫斯]合作设计出一种兼容黑白电视机的彩色电视方案而变得半出名。](https://www.google.com/patents/US2632058)

反射是递归算法的一部分，用于生成任意长度的格雷码。从最简单的格雷码开始:{0，1}。当然，它只是一个比特，但是每个条目之间的距离是一，所以它是一个格雷码。现在反转(反映)列表:{1，0}。还是格雷码。下一步是在第一个列表编号前放一个零，在第二个列表项前放一个一，然后连接这两个列表:{ 00，01，11，10 }。

你可以重复这个过程来得到你想要的位数。三个位将以列表{00，01，11，10}及其映射{10，11，01，00}开始。最后的代码是:{ 000，001，011，010，110，111，101，100 }。

当然，那只是一种可能的格雷码。还有其他有用的变体，名称从单调格雷码到“盒子里的蛇”码。你不能编造这些东西。

这些年来，我们已经看到了许多定制编码器,使用全格雷码通常是多余的。例如，如果你只关心方向和距离，你通常使用正交输出的旋转编码器。如果你只是想看看如何用 ARM 处理器读取这种类型的编码器，我们刚刚做了[其中一个](http://hackaday.com/2017/01/11/encoders-spin-us-right-round)。但是当绝对位置很重要，并且你关心保持过渡不变得太混乱时，格雷码是你需要的。