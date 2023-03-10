# 阿尔杜伊诺一路向下

> 原文：<https://hackaday.com/2018/02/26/moltoduino-arduinos-all-the-way-down/>

越来越难找到只有一个 CPU 的台式机或笔记本电脑。即使是典型的基于 ARM 的计算机现在也可能有多个内核。当然，没有什么可以阻止你一起使用多个微控制器，比如 Arduino。为了让这个过程更简洁，[Dimitris Platis]组装了[Moltoduino](https://platis.solutions/blog/2018/02/22/moltoduino-extra-cores-hil-testing/)，本质上是一个 Arduino 在一个盾牌上，用来插入另一个 Arduino。是的，他们会叠加。你可以在下面看到一个关于开源板的视频。

关键是电路板如何将引脚连接到易于在电路板之间跳线的连接上。有几个明显的用例，但[Dimitris]特别感兴趣的是硬件在环测试。这个想法是，你可以在一台计算机中使用一个模拟的 I/O 设备与被测软件交换假数据。

例如，你可能正在制作一个可以读取温度并控制加热器的真空吸尘器。第二台计算机可以代替温度传感器和加热器。您可以记录输出，也可以控制输入。当您想要建立可重复的测试用例时，这真的很好。

当然，你不一定要把这些板子堆叠起来才能工作。其实不一定要用另一个 Arduino。PC 或其他控制器可以作为替代测试设备。但是把它们都放在一个堆栈中是很方便的。在该项目的 [GitHub](https://github.com/platisd/moltoduino) 页面上有几个使用模拟硬件进行测试的例子。测试对象是一辆机器人汽车和一个超声波装置。

一个很好的特点是每块板都有一个开关，使主 Arduino 能够对它进行 ISP 编程。因此，虽然您可能不需要堆叠电路板来使用任何建议的技术，但它确实有助于实现一个漂亮而紧凑的封装。

通常，当我们看到一个集群时，它使用 [Raspberry Pis](https://hackaday.com/2017/10/11/terrible-cluster-of-pis/) 。或者，有时候， [PCs](https://hackaday.com/2017/03/16/super-computing-with-mini-itx-cluster/) 。

 [https://www.youtube.com/embed/VxhwocOEuLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/VxhwocOEuLs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

