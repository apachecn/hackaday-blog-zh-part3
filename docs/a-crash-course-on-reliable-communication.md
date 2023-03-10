# 可靠通信速成班

> 原文：<https://hackaday.com/2018/06/14/a-crash-course-on-reliable-communication/>

或许可以说，任何阅读这些文字的人都从概念上理解了物理连接的设备是如何相互通信的。在最基本的配置中，一根导线建立一个公共接地作为共享参考点，然后通过第二根导线发送“信号”。但是实际上*是一个信号，设备如何保持同步，当一个不可靠的链接导致一些数据丢失时会发生什么？*

[![](img/a012e866df555b374f80538cc9a8e5af.png)](https://hackaday.com/wp-content/uploads/2018/06/data_detail.png) 所有这些问题，以及更多问题，都在[【食本者】关于数据传输的精彩系列](https://github.com/beneater/error-detection-videos)中得到解答。他采用一种非常低级的方法来解释通信的基础知识，从不归零编码的概念开始，一直到共享时钟信号，以确保网络中的所有设备步调一致。我们大多数人都熟悉 I2C 等串行通信协议中使用的数据和时钟线，但很少有人能如此清晰详细地解释其工作原理。

他演示了让两个独立的设备进行通信的挑战，徒劳地试图调整接收和传输 Arduinos 的延迟，以尝试建立一个每秒 5 位的可靠链接。但是，即使以这种数字蜗牛的速度，错误也会在几秒钟内出现。[Ben]继续指出，消费电子产品中使用的振荡器在设备之间不够一致，无法在几百位以上保持同步。直到原子钟成为 Arduino 的标准配置，它才不是一个选项。

[Ben]然后解释了专用时钟信号的概念，以及如何使用它来确保设备同步，即使它们的本地时钟发生漂移。正如他所展示的，只要数据信号和时钟信号同时发生，实际的时序并没有太大关系。即使在这个基本演示的范围内，也会观察到时钟信号的一些漂移，但这对通信没有不利影响。

在本系列的下一部分中，[Ben]将讨论纠错技术。在那之前，你可能想看看[埃利奥特·威廉姆斯]在 I2C 上的精彩片段。

【感谢乔治·格雷夫斯的提示。]

 [https://www.youtube.com/embed/eq5YpKHXJDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eq5YpKHXJDM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

