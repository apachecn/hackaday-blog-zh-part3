# 在精神控制的特斯拉里思考你的工作方式

> 原文：<https://hackaday.com/2016/11/18/think-your-way-to-work-in-a-mind-controlled-tesla/>

当你拥有一辆价值 80，000 美元的汽车时，一个正常人可能倾向于永远不把它拿出车库。但是正常通常不是我们在这里所做的，所以看到由精神控制驱动的特斯拉只是稍微令人震惊。

[Casey_S]似乎是有问题的特斯拉 S 的所有者，但如果他不是，他将有一些“解释”要做。上周，他把装在汽车形状的盒子里的巨大电池和电脑带到伯克利的一个黑客马拉松上，并迅速给它安装了远程驾驶汽车所需的装置。是的，Model S 内置了转向电机，但特斯拉一直没有提供访问这些功能的 API。所以[Casey_S]和他的团队不得不从一个挡风玻璃刮水器电机和一个安装在 2x4s 框架上的电位计拼凑出一个转向伺服系统。线性致动器连接到刹车和油门踏板上，一切都与 Arduino 对话。

真正有趣的部分是，整个事情是由一个脑电图头盔和一个机器学习算法控制的，该算法可以检测驾驶员何时认为“向前”或“向右转”。它将这些想法转化为驱动执行器的变量。不幸的是，空间限制使[Casey_S]无法真正测试该装置，但休息后的视频显示，该系统工作良好，足以推动汽车前进并稍微转向。

以前这里没有太多的思想控制汽车，但我们已经介绍了[一个带有脑电图接口的轮椅](https://hackaday.com/2010/12/10/eeg-the-locomotion/)。

 [https://www.youtube.com/embed/gDIeaMl9fPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gDIeaMl9fPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

