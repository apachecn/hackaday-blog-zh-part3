# 量化廉价 RC 发射器的延迟

> 原文：<https://hackaday.com/2018/02/26/quantifying-latency-in-cheap-rc-transmitters/>

对于刚刚涉足 RC 领域的人来说，像 Flysky FS-i6S 这样的低成本发射机可能非常吸引人。但是买一个便宜的发射机会让你自己失败吗？RC 社区的普遍感觉是，更便宜的发射机在输入上有更高的延迟或“滞后”，这正是以 40+英里/小时的速度飞行时要避免的事情。因此，普遍的看法是，你的发射机是一个你不想廉价出售的领域。

[![](img/5f4c0d4ec98f6afe5473f77737f4fbf6.png)](https://hackaday.com/wp-content/uploads/2018/02/rclag_detail2.png) 为了验证这一理论，【马雷克·巴琴斯基】着手[比较 Flysky FS-i6S 和更成熟的 Taranis X9D](https://www.reddit.com/r/Multicopter/comments/7zjzam/i_measured_the_lag_on_a_cheap_flysky_radio_and/) 的响应时间。在休息后的视频中，他使用他的 Saleae 逻辑分析仪来计时发射器杆的运动在接收器处被解释为伺服命令需要多长时间。

[Marek]将逻辑分析仪直接连接到两个变送器的万向节上，使他能够在电子设备进行任何处理之前看到用户输入。看到万向节的平滑模拟曲线如何转换为“阶梯”数字输出特别有趣。

延迟测试的最终结果相当令人惊讶。简单地说:更便宜的 Flysky 收音机不仅能更准确地解释用户的输入，而且比 Taranis 快得多。[Marek]说他对这些结果感到非常惊讶，所以他重新进行了三次测试来验证。

但是，即使考虑到廉价收音机的明显更高的保真度，他警告说，你还不应该交换你的设备。高端发射机具有许多其他特性，这使得它们值得继续使用，即使新一代的无线电稍快一些。从这个视频中真正学到的是，如果你刚刚进入遥控游戏，这些便宜的发射器不一定是社区所说的死亡之吻。

像这样的实验和最近对普通业余爱好汽车的详细分析显示了人们对遥控世界的重视程度。这个单独的实验不太可能平息[关于“廉价”RC 发射器](http://hackaday.com/2017/11/20/can-commodity-rc-controllers-stay-relevant/)的争论，但也许这是一个开始。

 [https://www.youtube.com/embed/tsTZJim1LbY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tsTZJim1LbY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

