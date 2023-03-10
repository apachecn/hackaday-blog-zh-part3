# “看门狗”启发黑客无人机起飞

> 原文：<https://hackaday.com/2018/05/27/watch-dogs-inspired-hacking-drone-takes-flight/>

他们说，生活模仿艺术，用现代的说法，这基本上意味着如果你在视频游戏、电影或电视节目中看到一些很酷的东西，你可能会倾向于尝试并构建自己的版本。自然，这些东西通常以简单道具的形式出现，也许偶尔会嵌入 LED 或噪声产生电路。这并不是说你真的可以从《星际迷航》里造出一个相位器或者一个内部更大的电话亭。

[![](img/014cd4978e36e0933301586f5a2cab65.png)](https://hackaday.com/wp-content/uploads/2018/05/hakdrone_detail.jpg) 但在看到视频游戏*看门狗 2* 中的黑客四轴飞行器后，[【Gly tch】受到启发，开始着手现实世界版本的工作](http://glytch.tech/Watch-Dogs-Inspired-WiFi-Pineapple-Drone/)。它看起来不太像游戏中的无人机，但这不是重点。这个想法是为了看看一个小型飞行穿透测试平台在目前的技术下有多实用，从最终的构建来看，我们可以说他得到了他的答案。

所有的飞行电子设备都是现成的四轴飞行器齿轮。它运行在 Betaflight OMNIBUS F4 Pro V2 飞行控制器上，前部安装了 M8N GPS，用 DYS F20A ESC 控制 2006 年的 2400 千伏电机。有趣的是，[Glytch]正在试验使用 LG HG2 锂离子电池为 quad 供电，而不是更传统的锂聚合物电池，尽管他提到这两种电池技术之间的电压曲线存在一些问题。

但这场表演的真正明星是有效载荷:Hak5 菠萝纳米。由于菠萝本身提供了一个交钥匙渗透测试平台，[Glytch]只需要一种安全携带它并保持供电的方法。定制的框架使它保持舒适，DYS F20A ESC 上的 5 伏电池消除器电路(BEC)结合一个母 USB 端口允许为菠萝供电，而不必进行任何硬件修改。

在之前，我们已经见过配备数字武器的四轴飞行器，尽管没有你想象的那么多。但是随着[玩具级四轴飞行器变得越来越有能力](https://hackaday.com/2017/12/18/frankendrones-toy-quads-with-a-hobby-grade-boost/)，我们想象空中黑客革命并不遥远。

 [https://www.youtube.com/embed/lKtKYhTO5wk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lKtKYhTO5wk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

