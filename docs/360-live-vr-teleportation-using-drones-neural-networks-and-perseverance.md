# 360 直播 VR 瞬移使用无人机、神经网络、毅力

> 原文：<https://hackaday.com/2018/05/30/360-live-vr-teleportation-using-drones-neural-networks-and-perseverance/>

在过去的这个学期里，我在已经排得满满的数学和工程课程中加入了研究，就像任何受虐狂学生都渴望的那样。除了紧凑的日程安排，你怎么能错过实现实时 360 度虚拟传送到世界任何地方的机会呢？是的，它确实是和崇拜星际迷航的传送器一样的概念，只是少了亲临现场的能力。也许我们可以在关机的时候加上一个“把我传送上去，斯科特”的命令。

我工作的研究实验室是沉浸式通信(LION)实验室(T1)。它是由国家科学基金会、微软和 Adobe 资助的，并且已经研究虚拟现实传送有一段时间了。这里有很多很酷的技术在工作，比如无人机被用作位置收集设备。一个无人机网络将调查世界上任何地方的景观，并建立在虚拟现实中重建它所需的收集资产。好吧，一大群无人机一开始可能看起来有点吓人，但新兴技术什么时候不吓人了呢？

## 通过最小化未被查看的内容来提高速度

在 360°视频中，各种网格可以覆盖整个视口，如上图所示。这个网格可以被分成一定数量的相关空间块，这在捕捉用户的头戴式显示器(HMD)时变得更容易接受。这个初始网格允许我们集成相对用户视图导航模式，以创建一个视图端口驱动的率失真优化 360°视频流框架。

这显然是为了最大限度地提高用户在 360°视频使用期间的体验，同时在给定的网络和系统资源下尽可能保持运行时间的效率。我们集中精力做了两个 360 视频。在拥有用户 HMD 的大数据集后，动态热图被生成，其捕获导航到重叠网格的不同瓦片的可能性。这种视觉效果有助于看到多个用户分享的每个视频中的不同趋势。正如预期的那样，在测试的两个视频中，用户视野中心的区块是最常被查看的。人类是懒惰的生物。

比特率的率失真也是这个项目的一个组成部分，尽管我在这方面参与较少。360°视频流的一个已知问题是，传统上必须将整个 360°视野传递给用户，以减少模拟器和/或晕动病。然而，我们没有加载整个 360°球体，而是对 360°视频进行了编码，以最小化分配给我们生成的热图中不经常导航的各个 360°区域的数据速率。

优化效率是贯穿整个项目的压力。最终目标是有一个[神经网络](https://hackaday.com/2017/05/22/wrap-your-mind-around-neural-networks/)，可以接受它在注册用户视频中使用的训练，然后将其转移到相同用户的直播视频中。

 [![Roller Coaster Video](img/cd5459c903c3e345b394078f40f4eeba.png "Accuracy_Roller_Coaster")](https://hackaday.com/2018/05/30/360-live-vr-teleportation-using-drones-neural-networks-and-perseverance/accuracy_roller_coaster/) Roller Coaster Video [![Wingsuit Video](img/52fe7f171771f97213122d2e63ed0703.png "Accuracy_Wingsuit")](https://hackaday.com/2018/05/30/360-live-vr-teleportation-using-drones-neural-networks-and-perseverance/accuracy_wingsuit/) Wingsuit Video

在这两个视频中，我们将所提出的优化与右侧的基于速度的速率和整体速率进行了比较。在所有三种方法中可以看到相同的模式，但是所提出的方法具有最好的全面质量。

## 技术方法

我有一个不同想法的大杂烩，试图通过处理各种用户的 HMD 来优化 360 VR 视口数据。简单地说，过去用户的 HMD 理论上会给出足够的信息来可靠地预测在特定视频的某个时间段内视口中的哪个(哪些)区块需要更高的分辨率。通过用一组图片(GOP)中每一帧的偏转、俯仰和滚动来训练神经网络，目标是能够准确预测用户接下来会看哪里。更简单地说，当时间作为一个变量考虑时，HMD 输出本质上是一个用户焦点精确位置的矢量。

![](img/9d9b8c21ec40def7a5663e5c4a613a93.png)

**Visual representation of azimuth and polar angles in spherical coordinates with HMD**

我们尝试的第一种方法是在 MATLAB 中使用具有外源输入(NARX) 的[非线性自回归网络中的](https://www.mathworks.com/help/nnet/ug/design-time-series-narx-feedback-neural-networks.html)[时间序列预测](https://www.mathworks.com/help/nnet/gs/neural-network-time-series-prediction-and-modeling.html)。我们最初使用 HMD 的偏航和俯仰作为输入——很快发现，在这两个视频中，滚动远不如偏航和俯仰重要，因为它在整个显示中具有相对恒定的速率。然后，我们想到将图像数据添加到时间序列网络中，简单地看看它是否对时间序列网络产生了积极的影响，或者没有任何变化。将图像数据添加到 NARX 网络时出现了几个问题，但最持久的问题之一是如何正确格式化这些血腥的图像。我们所有的图像数据都在 32×32 单元阵列(帧)的 1×60 单元阵列(GOPs)中。可以理解，这不能作为网络的输入。与单一值的偏航和俯仰序列不同，我们有一个图像序列，其值存储为矩阵。我们寻找不同的方法来输入图像数据，以潜在地改善时间序列，但遗憾的是，在看似短暂的学期嘎然而止之前，我们的时间用完了。

深度学习目前最经典的用途之一是[图像分类](https://hackaday.com/2016/07/08/neural-network-targets-cats-with-a-sprinkler-system/)(思考识别)。我们感兴趣的是用一个预先确定的网络 [GoogLeNet](https://www.mathworks.com/help/nnet/examples/classify-image-using-googlenet.html) 训练我们的数据，使用图像分类作为一个新的角度来实现帧数据。想法是将视频分成每一帧，收集每一层的信息，然后将偏航和俯仰数据添加到[卷积神经网络(CNN)](https://www.mathworks.com/solutions/deep-learning/convolutional-neural-network.html) 的最后两层。不幸的是，我们没有一个实际支持 GoogLeNet 的 MATLAB 更新版本。该死的钱包。

如果我们能够完成测试，我们计划另外尝试使用隐马尔可夫模型进行预测。无论你是否碰巧赶上了这些天酷孩子正在做的机器学习， [Markov](http://www.zachwhalen.net/posts/twitter-bots-markov-chains-and-large-slices-of-clarity/) 是一个听起来肯定很熟悉的名字。完成所有这些不同的预测后，比较结果，看看哪种方法对我们的研究最有效，这将是非常有趣的。

## 继续研究

![](img/ac9bd8a498b66a3539c9aadca1312fc9.png)

从无人机网络发送给用户的特定景观的重建质量将取决于当前正在研究的许多因素。在不久的将来，可以利用群体配置优化路径规划的机器学习也将成为重中之重。这是最前沿的研究，当我秋天回来的时候，我希望能够加入其中。对于这个技术领域来说，这是非常令人兴奋的。

和任何研究一样，你遇到的障碍比突破要多。显然，实时 HMD 预测仍然需要改进。然而，每一个有价值的发明家/科学家/黑客都在他们智力生涯的某个时刻经历过这种看似暗淡的成功进展。好的人永远不会停止尝试。

我希望所有我有幸在实验室一起工作的学生在他们的研究中好运。我还想特别感谢雅各布·查卡雷斯基给我机会参与他的研究。