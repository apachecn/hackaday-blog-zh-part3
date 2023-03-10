# 电击计时器将加速卡坦殖民者的每场游戏

> 原文：<https://hackaday.com/2016/08/08/electroshock-timer-will-speed-up-every-game-of-settlers-of-catan/>

当轮到你的朋友没完没了地深思熟虑时，玩卡坦殖民者的乐趣只能与揍他们的欲望相匹配。[阿尔法凤凰]通过建造卡坦的[定居者:电击疗法资料片](https://www.youtube.com/watch?v=RGm3B0_0HeM)解决了低效游戏的困境。

[Alpha Phoenix]对该设备的细节有所保留，以防止有人在家中尝试这种设备并伤害自己或他人，但从他对该设备如何工作的分析中可以收集到很多信息。一个 Adafruit Trinket 微控制器连接到一个单极 12 掷开关——从一个双极 6 掷旋转开关修改而来——以选择最多六个不同的玩家(其他六个位置交替作为暂停空间),电击通过一个简单的电极传递，该电极由一根热粘合到牛奶罐的 HDPE 塑料上的导线制成。该电源能够提供高达 1100V 的电压，但实际输出远低于此，这要归功于其约 2.5M 欧姆的内置阻抗，以及[Alpha Phoenix]增加的电阻。

为了定义什么是“长回合”，饰品会计算最多前 100 个回合长度的平均值(而不是一个静态计时器来适应每场比赛中玩家的相对技能)，并电击任何违规的玩家——然后在设定的时间重复——以提醒他们需要加快速度。

 [https://www.youtube.com/embed/it1gvTxYi0s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/it1gvTxYi0s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Alpha Phoenix]提出了一个替代选项，蜂鸣器会响起，提示慢性子的人丢弃卡片作为惩罚，但这听起来远没有那么令人兴奋。无论你希望如何改进你的游戏——无论是通过[激光切割你自己的棋盘](http://hackaday.com/2015/02/28/laser-cut-settlers-of-catan-board-best-christmas-gift-ever/)还是[创造你自己的控制台](http://hackaday.com/2016/07/13/lightweight-game-console-packs-a-punch/)——只要记住保持安全和享受乐趣。

[通过[/r/电子](https://www.reddit.com/r/electronics/comments/4rco0v/this_catan_board_shocks_people_who_take_long_turns/)