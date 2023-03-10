# 用你的神经冲动移动一只机械手

> 原文：<https://hackaday.com/2016/12/31/move-a-robotic-hand-with-your-nerve-impulses/>

我们中的许多人都见过通过从人的神经或大脑中检测到的电脉冲来操作机器人或假肢。以这样或那样的形式，它们是大众市场技术新闻报道和科幻小说的主要内容。

然而，电视记者和科幻作家未能解决的问题是:它是如何工作的？简单来说，他们可能会说，单个神经的信号就像织布机中的电线一样被拾取，并被发送到假肢。但这是给孩子们的解释，很明显，在皮肤上安装几个电极是不可能的。他们*真的*是怎么做到的？

[Bruce Land]的康奈尔大学学生[Michael Haidar]、[Jason Hwang]和[Srikrishnaa Vadivel]的一个项目试图回答这个问题。他们已经建立了一个界面，允许他们使用从放置在他们前臂的电极收集的信号来控制机械手。他们的文章非常吸引人，因为在这个项目中存在大量的挑战，而手本身只是他们用现成的工具包解决的一个小问题。

接口本身必须解决拾取极其微弱的神经脉冲的问题，同时避免来自电源嗡嗡声和荧光灯的干扰。他们详细介绍了滤波器设计，以及如何使用隔离电源来尽可能降低这种噪声。

即使有了完美的界面，他们仍然需要训练他们的软件来识别不同的手指运动。将两个电极的读数绘制成图表的坐标轴，他们能够绘制出与单个肌肉相对应的图表区域。最后，这个答案取代了“为了孩子”的解释。

有几个视频链接自他们的文章，但下面我们留给你的是一个在低噪声环境下进行的测试。他们发现他们的实验室噪音太大，无法可靠地演示所有手指的移动，我们认为除了他们最成功的演示之外，向您展示任何东西都是不公平的。但同样值得记住的是，到达那里有多难。

 [https://www.youtube.com/embed/OJQ8WAgjOOc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OJQ8WAgjOOc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这些年来，我们已经介绍了大量的机器人和[假手](http://hackaday.com/2016/06/08/the-hacker-is-the-future-of-the-prosthetic-hackers-helping-those-in-need/),但是我们很少介绍以这种方式控制的机器人，这是一个挑战。即使是那些有 T3 的 T2，通常也是由大脑控制，而不是神经控制，因此要复杂得多。我们赞扬这个团队取得的成就，我们希望其他人将继续他们的工作。