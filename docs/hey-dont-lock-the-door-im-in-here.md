# “哎！别锁门，我在这里！”

> 原文：<https://hackaday.com/2017/11/13/hey-dont-lock-the-door-im-in-here/>

那些以在电脑前工作为生的人大部分时间都很少发出声音。除非你是 clicky 机械键盘俱乐部的成员，否则你的工作时间是不容易被人注意到的，在这段时间里，人们可能会忘记你。使用[这款智能手机热点存在探测器](http://ficara.altervista.org/?p=3744)，您可以确保自己不会被忽视。

[Emilio Ficara]安静的工作习惯导致他的室友有时将他锁在里面，给他带来不便。PIR 或微波占位传感器可能已经解决了这个问题，只是几个弯曲的手指并不总是足以触发它们。幸运的是，[埃米利奥]也明智地不信任免费 WiFi，所以他的手机总是被设置为移动热点，这让他有办法可靠地检测到他的存在。一个 ATtiny2313 和一个 ESP-01 负责轮询他的电话的 SSID，并为他的室友闪烁他门旁边的亮蓝色 LED。当然，它并不完美；任何知道他的 SSID 的人都很容易伪造它。但简单的工作现在。

现在几乎每个人都带着一个，智能手机检测是一个人存在的很好的代理。但它并不是在所有情况下都有效，所以你可能想熟悉一下前面提到的 [PIR](https://hackaday.com/2009/08/21/passive-infrared-pir-sensor-tutorial/) 和[微波](https://hackaday.com/2017/05/24/radar-sensors-put-to-the-test/)方法。