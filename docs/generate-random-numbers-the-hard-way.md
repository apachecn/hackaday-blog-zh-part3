# 艰难地产生随机数

> 原文：<https://hackaday.com/2017/12/13/generate-random-numbers-the-hard-way/>

你的工作是创建一个随机数生成器。

你的设备从一个扬声器和一个薄膜开始。在这层膜上有一把大理石大小的小铜球。一个音频源向扬声器提供信号，并使球来回跳动。如果球弹得足够高，它将有机会从七根铜管中的一根下来。每个管道中的光学传感器检测球，并将数据输入 Ardunio Mega。当球到达管子的末端时，一只机器人手将拿起球，并将其放回扬声器薄膜上。当我们编写一个算法，使得扬声器的音频输出是有多少球掉进管道的函数时，神奇的事情就发生了。

以上是对[::vtol::]的美术作品:[动能随机数生成器](http://vtol.cc/filter/works/driver)的大致描述。我们很确定有更简单的方法来获得一些非确定性的比特，但是可能没有更多的乐趣来观看。

[::vtol::]是哈卡代航空公司的常客。你还会在哪里展示你的 [8 位游戏男孩照片枪](https://hackaday.com/2015/04/03/8-bit-digital-photo-gun/)或者你的[脑波激活铁磁流体怪兽浴池](https://hackaday.com/2014/10/03/art-from-brainwaves-antifreeze-and-ferrofluid/)？当你发现我们甚至报道了[他的另一个动态随机数发生器](https://hackaday.com/2017/09/01/follow-the-bouncing-ball-of-entropy/)时，你会感到震惊吗？有趣的东西！