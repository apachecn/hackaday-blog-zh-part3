# 作为监听设备的亚马逊回声

> 原文：<https://hackaday.com/2017/08/03/the-amazon-echo-as-a-listening-device/>

不可避免的是，在一款新设备发布后，会有一个关于其根源、逆向工程或其他暴露其黑客能力的声明。现在有问题的设备是亚马逊 Echo，因为 MWR 实验室宣布他们的工作是[说服 Echo 从麦克风产生现场音频，并将语音助理设备变成秘密监听设备](https://labs.mwrinfosecurity.com/blog/alexa-are-you-listening)。

这项工作依赖于亚马逊基于 Echo 的调试连接器的[先前发现和逆向工程](https://vanderpot.com/Clinton_Cook_Paper.pdf) (PDF)，该连接器暴露了 SD 卡接口和串行终端。在这项工作之后，他们能够获得设备的 root 访问权限，分析音频缓冲区的结构以及不同的 Echo 进程如何使用它们，并运行亚马逊自己的“shmbuf_tool”应用程序，以将原始音频数据传输到网络流。令人惊讶的是，这可以在不影响设备正常运行的情况下完成。

应该强调的是，这是一种需要物理接触设备和一些知识来执行的利用。但不难想象，它可以被制作成一个近乎自动化的过程，只需要一个带有一组弹簧针的设备与一个快速移除其外壳的 Echo 相匹配。

也就是说，不可避免地，在不久的将来，将会有足够多的未使用的 Echos 四处传播，它们的可寻根性将使它们对我们社区的人们有用。我们期待人们利用扎根回声提出什么有趣的项目。

这不是我们第一次讨论回声作为监听设备的使用。

Via [黑客新闻](https://news.ycombinator.com/item?id=14906254)。

亚马逊 Echo 图片:fastly[[CC BY-SA 4.0](https://commons.wikimedia.org/wiki/File:Amazon_Echo_1_2017-02-23.jpg)。