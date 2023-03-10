# 世界上最小的小提琴使用雷达和机器学习

> 原文：<https://hackaday.com/2016/06/15/worlds-tiniest-violin-using-radar-and-machine-learning/>

[Design I/O]的人想出了一种方法，让你通过摩擦手指来弹奏世界上最小的小提琴，并让它发出小提琴的声音。对于那些不知道的人，当你想对某人的抱怨表示假装的同情时，你可以摩擦你的拇指和食指，说“你听到了吗？这是世界上最小的小提琴，它只为你演奏”，只不过现在他们可以听到小提琴的声音，而你的手势可以控制音量和播放。

[设计 I/O]结合了一些技术来实现这一点。第一个是谷歌的 Soli 项目，一个芯片上的微型雷达。Soli 项目的目标是通过使用微型雷达进行无接触手势交互来消除物理控制。例如，将拇指滑过伸出的食指，可以被解释为移动滑块来改变某个东西的数值，也许是打开汽车的空调。看看谷歌下面关于他们的雷达和手势的很酷的演示视频。

Project Soli 的雷达是另一项有趣技术的输入端:[Wekinator](http://www.wekinator.org/)，这是一款面向艺术家和音乐家的免费开源机器学习软件。[他们网站上的例子](http://www.wekinator.org/walkthrough/)描绘了一幅激动人心的画面。你给 Wekinator 输入和输出，然后告诉它训练它的模型。

这种情况下的输出端是小提琴音乐。输入是雷达探测到的任何东西。Wekinator 会帮你完成繁重的工作，只需像雷达监测手指运动一样给它输入，它就会学习你选择的手势，并执行适当训练的输出。

[设计 I/O]可能不仅仅使用 Wekinator 的前端，因为他们也使用 openFrameworks，一个开源的 C++工具包。Wekinator 的另一个有趣之处是他们使用[开放式声音控制(OSC)](https://en.wikipedia.org/wiki/Open_Sound_Control) 协议通过网络进行通信，以获取其输入和输出。您可以在下面的视频中看到[Design I/O]的最终结果。

如果你想要一个真正的微型乐器来演奏，那么我们建议[这款迷你电动尤克里里琴](http://hackaday.com/2014/11/05/create-a-buzz-with-the-mini-electric-ukulele/)，它可以放在你的手掌中，在其微型激光切割胶合板框架中包括微控制器、扬声器和电池。

[https://player.vimeo.com/video/155570863](https://player.vimeo.com/video/155570863)

 [https://www.youtube.com/embed/0QNiZfSsPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0QNiZfSsPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [GIZMODO](http://gizmodo.com/finally-a-playable-version-of-the-worlds-tiniest-violi-1781747202)