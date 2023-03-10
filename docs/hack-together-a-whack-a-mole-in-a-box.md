# 在盒子里拼凑一只打地鼠！

> 原文：<https://hackaday.com/2017/09/02/hack-together-a-whack-a-mole-in-a-box/>

这里有一个项目，你可以在一个下午内完成，前提是你手头有零件，而且一定会很有趣。Hackaday.io 用户[ SunFounder]带领我们经历了将一个不起眼的[纸箱转变成一个打地鼠游戏](https://hackaday.io/project/25973-how-to-diy-a-whack-a-mole-game-with-cardboard-box)的过程，这可能正是释放压力或吸引附近任何孩子的门票。

一个多控制板和九个街机按钮是这里的关键硬件，电线和 USB 电缆完成了其余的电子设备。将按钮芯与上壳分离，将外壳安装在盒子中，并将按钮芯的 LED 阴极连接到按钮的 on 端子。重复八次。并联焊接按钮，并在按钮的端子上增加一些电线，以延长它们的触及范围。再重复八次。

将完成的 LED+核心放入按钮中，并将它们的 ON 端子连接到多功能控制板上各自的按钮。现在是艰难的一步:使用迷你 USB 转 USB 电缆将控制器连接到你想用来在 Arduino IDE 中运行[游戏代码](https://github.com/sunfounder/SunFounder_Multi_Control)的计算机。修改键映射就可以了！休息之后，请观看构建视频。

 [https://www.youtube.com/embed/KJxi6EA8qF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KJxi6EA8qF4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



树莓 Pi 和小 LED 屏幕，甚至是[图形计算器](http://hackaday.com/2016/01/25/the-newest-graphing-calculator-game/)之类的东西会让这款游戏更便携，但不可否认的是，在电源方面会更复杂一些。当然，总有选择把这个游戏带到一个[更困难的极限](http://hackaday.com/2015/08/04/engineers-create-super-hard-whack-a-mole/)。