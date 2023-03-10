# 被 Arduino 和多个 RFID 阅读器控制

> 原文：<https://hackaday.com/2018/05/13/held-captive-by-arduino-and-multiple-rfid-readers/>

如果你是那种有朋友的人，或者时不时离开地下室的人，我们听说这些“密室”风靡一时。基本上，你和其他几个人被锁在一个房间里，必须解决各种问题和难题，直到你最终取得足够的进展，他们才会让你出来。这实际上听起来很像 Hackaday 总部的工作条件，只是他们偶尔会从门缝里塞些披萨给我们，这很好。

[![](img/e228a344137ba108b376bf7366ca0a85.png)](https://hackaday.com/wp-content/uploads/2018/04/multirfid_detail.jpg) 在这种轻松愉快的人质事件中，无论你站在哪一边，由【安娜娜】发明的[多标签 RFID 锁都会派上用场。通过将多个 MFRC522 RFID 读取器连接到一个 Arduino Uno，她想出了一种只有在 RFID 标签的适当组合已经排列好时才触发设备(如电子门锁)的方法。只要有一点点想象力，这就允许出现一些非常复杂的谜题场景，这些场景一定会让你的囚犯着迷，直到你可以把乳液降低到他们身上。](https://github.com/Annaane/MultiRfid)

她的代码允许你配置触发 Arduino 的一个数字引脚所需的 RFID 卡的类型和数量，这些数字引脚通常会连接到一个继电器，以启动你想要的任何设备。Arduino 草图还设置为通过状态 LED 给玩家“提示”:快速闪烁让你知道扫描的标签是错误的，慢速闪烁意味着你还没有足够的扫描。

休息后的视频显示了该构建的一些亮点，以及如何使用 RFID“组合”和手动超越来触发附加继电器的快速演示。

[黑客确实热爱 RFID](https://hackaday.com/2016/04/17/rfid-lock-keeps-your-bike-safe/) 。使用它们进行[物理访问控制](https://hackaday.com/2016/09/25/simple-rfid-door-lock-system/)是围绕这些部件的[相当常见的项目，我们甚至已经看到了](https://hackaday.com/2014/07/18/quick-and-dirty-rfid-door-locks-clean-up-nice/)[类似的数字领域](https://hackaday.com/2018/03/17/rfid-unlock-your-pc-because-youre-1337/)的设置。

 [https://www.youtube.com/embed/ahc8Yai_sWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ahc8Yai_sWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

