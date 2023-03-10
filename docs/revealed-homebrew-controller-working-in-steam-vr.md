# 透露:家酿控制器工作在蒸汽 VR

> 原文：<https://hackaday.com/2016/12/16/revealed-homebrew-controller-working-in-steam-vr/>

[Florian]一直在 VR 控制器方面投入大量工作，这些控制器可以在不干扰常规鼠标+键盘组合的情况下使用，他最近的工作为[在 Steam VR 中成功模拟一个 Vive VR 控制器](http://flrnmrr.com/2016/11/30/arduino-vive-controller-emulation)打开了大门。他在手上使用基于 Arduino 的定制硬件 Leap Motion 控制器，并将数据融合到软件中。

我们之前已经看到过[Florian]的工作，成功地将跳跃动作与额外的硬件传感器结合起来。这个想法是为了补偿 Leap Motion 传感器不太擅长检测某些类型的运动，例如将拳头朝着或远离自己倾斜——这种运动类似于将枪向上或向下瞄准。与此同时，一个重要的目标是，任何添加的硬件都可以腾出手指和双手。

[![emulation-demo-optimized](img/3432faf3c7c196905cd72305ddcaf585.png)](https://hackaday.com/wp-content/uploads/2016/12/emulation-demo-optimized.gif) 【弗洛里安】的 DIY 虚拟现实手控模仿了 Valve 的 Steam VR 跟踪中的 HTC Vive 控制器，带有一个与他的定制硬件配合工作的软件链。他的 DIY 控制器不需要主动握住，因为根据设计，它可以抓住手，让手指自由地做其他任务，如打字或打手势。

上次我们看到[Florian]的工作时，开发仍然很繁重，没有任何源代码共享，但是现在有了一个项目的 [git 库](https://github.com/fmaurer/FreePIE-VR-Controls),里面有你需要的一切来享受乐趣。他补充道，“我看到很多玩 Wii 双截棍的人都想这么做。只需对我的 FreePIE 脚本进行一些编辑，他们应该可以轻松地启用他们想要的任何按钮/方向数据。”

 [https://www.youtube.com/embed/S1-FHn2ySXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/S1-FHn2ySXA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们有在软件中模拟 Vive 控制器的 DIY 硬件，并且我们已经看到[通过 DIY 电子设备](http://hackaday.com/2016/07/06/using-the-vives-lighthouse-with-diy-electronics/)与 Vive 的 Lighthouse 硬件接口。这个领域有很多黑客活动，看到接下来会发生什么令人兴奋。