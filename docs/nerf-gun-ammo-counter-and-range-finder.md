# Nerf 枪弹药计数器和测距仪

> 原文：<https://hackaday.com/2017/09/02/nerf-gun-ammo-counter-and-range-finder/>

DIY 电子产品运动所允许的分线板的扩散是惊人的。买几块不同的板，把它们连到一个微控制器或信用卡电脑上(两者都在各自的分线板上)，写一点代码，你就能创造出一些真正有趣的东西。以 Reddit 用户[Lord_of_Bone]的 [Nerf 枪械弹药计数器和测距仪](https://314reactor.com/2017/08/15/nerf-gun-ammo-counter-range-finder/)为例，这是一个拥有伟大想法并四处寻找实现方法的伟大例子。

对于测距仪，[骨之王]依靠超声波测距仪。对于弹药计数器，[骨之王]选择了一个接近传感器。为了运行一切，使用了 Raspberry Pi Zero，视觉效果由彩虹帽提供。测距仪是不言自明的。接近传感器位于枪的枪口末端，当它检测到一个 Nerf 飞镖经过时，它会将弹药数减一。Blu-tack 用于固定一切，但[骨之王]计划在原型阶段过后使用 Sugru。

[骨王]的一个问题是没有办法知道弹匣里有多少 Nerf 子弹。当前持用者必须在重装弹药时按下按钮将数量重置为预设数量。我们确信[骨之王]会感谢那些一天黑一次的人提供的任何建议。

[Lord_of_Bone]提供了完整的材料清单、Python 代码、大量图片和逐步说明，以便您也可以确定您的目标有多远，以及您是否有足够的弹药来击中它们。我们在网站上有相当多的 Nerf 模块，[骨之王]可以看看[这篇关于如何跟踪你的 Nerf 弹药](https://hackaday.com/2014/07/09/upgraded-nerf-gun-keeps-track-of-your-ammo/)的文章，[这里有一个不同的方法来确定一个 Nerf 飞镖是否已经发射](https://hackaday.com/2016/05/05/35-mph-nerf-darts/)(并测量它的速度。)

【via[Reddit】](https://www.reddit.com/r/raspberry_pi/comments/6twyd4/nerf_gun_ammo_counter_range_finder_with_a/?st=j6e63crm&sh=2ed8d531)

 [https://www.youtube.com/embed/e9PPDWMXrEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e9PPDWMXrEs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

