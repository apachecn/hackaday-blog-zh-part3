# 紧凑型控制器自动百叶窗

> 原文：<https://hackaday.com/2016/05/24/compact-controllers-automate-window-blinds-on-the-cheap/>

对于今天的自动化家庭来说，市售的电动百叶窗是一种不错的高端产品，但它们往往价格昂贵。对相当于齿轮马达和控制器的东西收取这么多费用似乎很愚蠢，这就是为什么[詹姆斯·威尔考克斯]亲自动手，想出了这个简单而便宜的无线盲人控制器。

[詹姆斯]以明智的方式开始了他的项目，对问题进行了透彻的分析。一旦 COTS 替代品被淘汰——六个窗口将是 1200 美元——他提出了一系列可交付成果，包括倾斜到预先确定的位置，跨多个窗口倾斜同步，以及长电池寿命。每个百叶窗顶部导轨上的硬件最终都变成了一个用于驱动器的定制 PCB 上的 Moteino，一个 2 美元的步进电机和一个 4 节 AA 电池组。一个百叶窗中的 Moteino 通过 USB 与一个 BeagleBone Black 对话，并通过无线方式与其他窗户进行协调控制。至于电池寿命，[詹姆斯]利用了 Moteino 的低功耗监听模式，将电流消耗减少了大约三个数量级，这应该相当于几年更换一次电池。他只花了大约 40 美元一个窗户。

百叶窗似乎是黑客攻击的一个诱人目标，无论是将普通百叶窗机动化还是将商业机动化单元连接到家庭自动化系统的 T2。我们喜欢这种紧凑的结构，并想知道它是否可以作为手动百叶窗的配件。

 [https://www.youtube.com/embed/l3H9lPdafEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l3H9lPdafEg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/4k8i3x/diy_motorized_blinds_for_40_with_arduino/)