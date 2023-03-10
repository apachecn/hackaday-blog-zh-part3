# 具有触觉反馈的无线机器人手爪

> 原文：<https://hackaday.com/2016/06/29/wireless-robotic-gripper-with-haptic-feedback/>

我们不确定[萨姆·鲍姆加滕]和[格雷厄姆·休斯]上的哪所“高中”给了他们工具，让他们能够如此出色地执行他们的[机器人手爪](https://www.youtube.com/watch?v=fGdjGD3bKH8)。我们知道它和我们的不一样。显然有些高中有 SLS 3D 打印机和 Solidworks。尽管如此，一个脾气暴躁、有三个手指的商店老师还是不停地卸下台锯的安全装置，并在油毡上刻有如此多阴茎和名字的木板上教授制图，而不是一半的挑战是不要将它们转移到线条作业上。

撇开我们的痛苦不谈，[山姆]和[格雷厄姆]制造了一个相当令人印象深刻的机器人手爪。事实上，在跟踪[山姆]的 linkedin 以确定他是老师还是学生之后，(学生)我们认为他们足够聪明，他们可能已经在一个山洞里用废料建造了它。就像[【同人】](https://hackaday.com/2016/06/16/homofaciens-shows-off-with-diy-paper-printer/)，还有[铁人](http://hackaday.com/2014/08/30/homemade-superhero-james-diy-exoskeleton/)。

手爪本身是三个大型业余伺服系统，通过连杆连接到手指上，都是 3D 打印的。机械手指在接触点有力传感器，控制手套在指尖有微型振动马达。当握力上升时，电机振动更强烈，提供有用的反馈。在下面的视频中，你可以看到他们用手爪表演了一系列相当精细的运动技能。

手爪用一些研磨带安装在一根柱子上，就是滑板甲板上的那种。在杆子的后面，电子设备和电池位于一个项目箱内。这为手的重量提供了平衡。

控制手套的手指背面有柔性电阻。arduino 对来自这些设备的信号进行处理，并通过 Xbee 模块将其传输给 gipper 中的伙伴 Arduino。

[山姆]和[格雷厄姆]做得很好。他们完成了当今专业工作中的所有设计阶段。从一张餐巾纸草图开始，他们转向数字原型，最终完成了一个按计划工作的组件。休息后的视频解释了它是如何工作的，还有一个演示视频。

 [https://www.youtube.com/embed/fGdjGD3bKH8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fGdjGD3bKH8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



警告:下面是 Dubstep

 [https://www.youtube.com/embed/d5VxvPQnacA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/d5VxvPQnacA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

