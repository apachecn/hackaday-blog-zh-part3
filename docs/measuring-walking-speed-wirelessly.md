# 无线测量行走速度

> 原文：<https://hackaday.com/2017/05/10/measuring-walking-speed-wirelessly/>

有很多方法可以尝试从数学上量化一个人的健康程度。静息脉率、血压和血氧合作用都很容易测量，可以用来预测各种临床结果。然而，你可能没有考虑到步态速度，或者一个人走路的速度。事实证明，步态速度是一种预测各种疾病发作的可行方法，如充血性心力衰竭或慢性阻塞性肺病。事实证明，当人们生病、年老或体弱时，他们往往会走得更慢——就像你最喜欢的 RTS 中的小机枪兵，当他们的生命值为红色时。但如何衡量这一点呢？麻省理工学院的 CSAIL 已经升级，有了一种完全无线测量行走速度的方法。

你可以在这里 (PDF)阅读论文[。WiGate 设备发出低功率无线电信号，然后测量反射信号，以确定一个人在一段时间内的位置。然而，光靠这些是不够的——重要的是具体测量行走速度，以避免例如一个人在看电视时不动而引发的假阳性。算法用于将行走活动从数据集中分离出来，允许设备在后台运行，记录行走速度数据，无需任何用户交互。](https://people.csail.mit.edu/cyhsu/papers/wigait_chi17.pdf)

这种形式的被动监测可以在疗养院中有很大的应用，那里的工作人员经常有大量的病人要监测。它将允许收集临床相关数据，而不需要任何人工干预；当病人的行走模式表明有更大的问题时，该设备可以简单地提醒工作人员。

我们在 Hackaday 看到了一些很棒的健康研究，比如这个开源心电图。休息后的视频。

 [https://www.youtube.com/embed/qCYrz7f0un4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qCYrz7f0un4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

