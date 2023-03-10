# 详细介绍特雷门琴

> 原文：<https://hackaday.com/2017/09/09/theremin-in-detail/>

【Keystone Science】最近[发布了一个关于制作特雷门琴](https://www.youtube.com/watch?v=oRhO0MJIl58)的视频——你知道，当你把手在它周围移动时，这种乐器会发出奇怪的哨声。电路非常简单(T2 借用了 T3)，但我们喜欢视频解释理论的方式，甚至深入到谐振频率背后的数学。

该电路使用两个场效应晶体管作为振荡器。一个 LM386 放大器([黑客最喜欢的](https://hackaday.com/2016/12/07/you-can-have-my-lm386s-when-you-pry-them-from-my-cold-dead-hands/))驱动一个扬声器，这样你就可以在没有外部设备的情况下使用仪器。初始构建是在试验板上进行的，但最终构建是在 PCB 上进行的，并且有一个外壳。

这是一种可以抓住孩子想象力的项目——尤其是对音乐感兴趣的孩子。我们并不反对微控制器项目，但像这样的电路非常适合探索振荡器、放大器、谐振频率和其他典型 Arduino LED 闪光灯无法获得的电子细节。

我们在过去讨论过很多问题，包括一些非常简单的问题。甚至有一个使用[红外传感器](https://hackaday.com/2016/03/21/the-infrared-theremin/)。

 [https://www.youtube.com/embed/oRhO0MJIl58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oRhO0MJIl58?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

