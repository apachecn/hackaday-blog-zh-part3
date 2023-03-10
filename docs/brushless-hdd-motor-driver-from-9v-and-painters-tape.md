# 9V 无刷硬盘电机驱动器和油漆工带

> 原文：<https://hackaday.com/2016/09/21/brushless-hdd-motor-driver-from-9v-and-painters-tape/>

硬盘的工作原理是旋转充满磁化数据的盘片，而读/写磁头可以根据需要快速获取或改变数据。旧的(或者更便宜的)驱动器转速为 5400 转/分，更好的驱动器转速为 7200 转/分，而精英驱动器(像你这样的人从不花钱购买)转速在 10k-15k 转/分之间。这种旋转是由于轴承和无刷 DC 电机的甜蜜组合。

不幸的是，没有无刷电机驱动器，你就无法驱动无刷电机。当然，这并不完全正确——而且[汤米·卡拉威]确实为这一规则拼凑了一个粗糙的例外。他正在用 9 伏电池和一些蓝色油漆工胶带来驱动无刷电机。

无刷电机的工作原理是在转子(旋转的部分)上放置永久磁铁，并在其周围放置多个固定线圈。然后，无刷电机驱动器以不同的仔细定时模式激励这些线圈，以相同的方向连续推动转子磁铁。

[Tommy]将他的 9V 连接到其中一个线圈上，观察到它将转子固定在适当的位置。然后，他开始尝试不同的方法，在适当的时候自动断开电路，切断线圈的电源。这意味着使用硬盘驱动器的旋转中心作为电路的一部分，用蓝色画家的胶带以交替的模式来创建时序。这是无刷电机驱动器，还是他只是重新发明了有刷电机？

如果这个工作台的小把戏让你想要一些硬核的 BLCD 动作，那么[这款 20 美元的产品](http://hackaday.com/2016/07/29/3-phase-bldc-motor-controller-will-run-you-20-in-parts/)可以以非常高的速度推动电机，你不会错的。

 [https://www.youtube.com/embed/e6XVDd4eHIQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e6XVDd4eHIQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[通过 [/r/ECE](https://www.reddit.com/r/ECE/comments/51ylki/power_a_brushless_hard_drive_motor_without_a/)