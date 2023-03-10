# 一部树莓派雨人正在制作中

> 原文：<https://hackaday.com/2017/10/13/a-raspberry-pi-rain-man-in-the-making/>

我们看到很多树莓 pi 被用来玩游戏，但这与最新的 RetroPie 版本完全不同。[这只树莓派正在学习如何阅读扑克牌](https://www.youtube.com/watch?v=m-QPjO-2IkA)，目标是成为终极算牌 21 点玩家。

如果[出租车司机]还没有把他的项目命名为[雨人](https://youtu.be/RW1qHA5Hqwc?t=8m7s)，我们谦恭地建议他这样做。因为能把圆周率算进六张牌的鞋子里是件了不起的事情，尽管在赌场附近这是绝对不允许的。算牌的第一个障碍是阅读它们，而[出租车司机]已经在 Pi 3 上利用 OpenCV 的能力完成了这项任务。他在下面的视频中的描述非常详细，但方法很简单:使用阈值和轮廓的组合在比赛场地的 PiCam 图像中找到卡片。然后，在纸牌被隔离的情况下，将旋转后的纸牌图像左上角的等级和花色与原型图像进行比较，以识别纸牌。Pi 提供足够的马力来快速识别任意数量的非重叠牌；我们假设[出租车司机]将不得不在某个时候解决使用不同字体的重叠卡片和套牌。

我们渴望有一天看到这个私家侦探玩 21 点。当他编写代码时，他可能想看看 21 点策略的[算法方法](https://hackaday.com/2013/01/15/evolutionary-algorithms-computes-the-best-blackjack-strategy/)，以及[击败庄家的真正几率](https://hackaday.com/2015/08/31/beating-the-casino-there-is-no-free-lunch/)。

 [https://www.youtube.com/embed/m-QPjO-2IkA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m-QPjO-2IkA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [r/Raspberry_Pi](https://www.reddit.com/r/raspberry_pi/comments/75ici2/i_made_a_raspberry_pipowered_playing_card/)