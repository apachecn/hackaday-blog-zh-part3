# 用状态机更清楚地陈述你的意图

> 原文：<https://hackaday.com/2018/04/06/state-your-intentions-more-clearly-with-state-machines/>

对于门外汉来说,“国家机器”这个词听起来像是大得吓人的复杂事物。它们不一定有用，但可能非常有用。事实上，状态机不是物理机器，而是流程的模型。它们将系统可能处于的状态与允许的转换联系起来。例如，媒体播放器在停止时可以切换到播放或打开另一个文件。在播放的时候，它可以去暂停，停止，倒退，快进等等。状态机创建所有状态及其连接方式的映射。它是一个抽象的工具，在实际编程之前提供了一个图形化的方法来组织你的代码。

在他的[视频](https://www.youtube.com/watch?v=v8KXa5uRavg&feature=youtu.be)中【Chris Guichet】使用一个状态机去抖一个开关，为初学者友好地介绍这个概念。然后，他展示了如何将手绘地图转化为实际代码，包括调试状态机的部分。

 [https://www.youtube.com/embed/v8KXa5uRavg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/v8KXa5uRavg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



国家机器是退伍军人容易使用的工具之一，但往往很难向年轻人解释清楚。这个视频解决了这个问题。对于那些喜欢阅读的人来说，我们手头有一份以文本形式提供的详尽解释。当然还有一台带[闪光灯](https://hackaday.com/2016/10/10/the-collatz-o-matic-a-state-machine-with-style/)的物理机器。