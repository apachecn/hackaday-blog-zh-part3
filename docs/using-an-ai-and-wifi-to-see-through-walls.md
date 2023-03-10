# 使用人工智能和无线网络来透视墙壁

> 原文：<https://hackaday.com/2018/07/02/using-an-ai-and-wifi-to-see-through-walls/>

现在不仅可以透过墙壁看到人们，还可以看到他们是如何移动的，如果他们在走路，还可以知道他们是谁。我们终于有了《全面回忆》原版电影中施瓦辛格走在《T3》后面的[人体扫描仪。](https://www.youtube.com/watch?v=7CX9Agzeh-c)

这是麻省理工学院计算机科学和人工智能实验室(CSAIL)一个小组的工作。穿透墙壁的部分是通过使用射频发射器和接收天线来完成的，这并不是很新。我们自己的【Gregory l . char vat】[在他的车库](https://hackaday.com/2015/04/07/build-a-phased-array-radar-in-your-garage-that-sees-through-walls/)里建造了一个令人印象深刻的相控阵雷达，它清楚地显示了墙后复杂形状的运动。新的是使用神经网络来更好地解读这些天线接收到的信号。神经网络给出了人们头部、肩部、肘部和其他身体部位的姿势估计，稍作进一步处理就可以将其转化为骨骼图。

他们以多种方式评估其准确性，所有这些都在他们的论文中有详细描述。最有趣的，或者可能是最可怕的方法是，看看它是否能通过每个人走路的方式来辨别谁是骨架人物。他们首先训练另一个神经网络来识别不同人的风格。然后，他们将姿势估计输出传递给这个风格识别神经网络，它以 83%的准确率正确地猜测出人们何时可见以及何时在墙后。这意味着他们不仅知道一个人在做什么，而且知道这个人是谁。

看看下面的视频，看看在各种条件下做各种事情的真人版和骨骼版的一些令人印象深刻的对比。看起来《全面回忆》中的科幻未来又近了一步。现在[如果我们可以殖民火星](http://hackaday.com/2017/08/17/living-on-mars-the-stuff-you-never-thought-about/)。

 [https://www.youtube.com/embed/HgDdaMy8KNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HgDdaMy8KNE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

