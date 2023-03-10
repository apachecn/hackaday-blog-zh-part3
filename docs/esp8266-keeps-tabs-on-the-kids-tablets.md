# ESP8266 监控孩子的平板电脑

> 原文：<https://hackaday.com/2018/07/05/esp8266-keeps-tabs-on-the-kids-tablets/>

假设你有一个孩子，并且不再受子宫的束缚，他们很有可能已经对 LCD 显示屏的发光之美有了一些体验；只有几个月大的婴儿经常被给予平板电脑或智能手机，让他们有事可做。但是，随着孩子到了能够外出或做一些更有建设性的事情的年龄，张着嘴、睁大眼睛盯着他们的平板电脑成了许多父母的担忧。

[![](img/47aea5aa5c68d133077d88dde4061bb5.png)](https://hackaday.com/wp-content/uploads/2018/06/tabtab_detail.jpg) 【理查德·加尔斯哈根】就是这样一位家长。他想要一种方法来监控他的孩子使用 iPad 的时间，所以[他想出了一个基于 ESP8266](http://www.instructables.com/id/IPad-Play-Timer/) 的自动化系统。它不仅可以跟踪平板电脑的使用时间，甚至还包括一个奖励系统，允许父母为良好行为增加额外的使用时间。

在最基本的层面上，该设备是儿童平板电脑的一种“皮套”。当药片放入槽中时，它会按下空腔底部的微型开关，从而停止计时器。当开关打开时，设备前面的 LED 显示屏会倒计时，ESP8266 会通过 IFTTT 向孩子的设备推送剩余时间的通知。

可以通过 RFID 卡将时间添加到时钟中。这些卡片是作为对良好行为、完成家务等的奖励而发放的。孩子只需要在系统前面通过卡来兑换它的价值。一旦卡被“用完”，父母可以用他们自己的特殊卡重置它。

这是一个非常巧妙的设置，完美地利用了 ESP8266。读取 RFID 卡，更新计时器，并使用 IFTTT 的 API 使这个小板子相当忙碌；[理查德]说它已经完全透支了。

你可能想知道当时钟到达零时会发生什么。嗯，根据休息后的视频…没什么。一旦时间用完，平板电脑上就会弹出一个通知，告诉他们把它收起来。有些人可能会认为这是一个错误，但据推测，这是人类接管养育工作并让 ESP8266 休息的系统的一部分。

这不是我们第一次看到一个微控制器被用来让小黑客们按计划进行。至少(到目前为止)他们中没有一个人在孩子们看着*黑镜*的时候开始[追踪](https://hackaday.com/2018/01/15/raspberry-pi-offers-soulless-work-oversight/)。

 [https://www.youtube.com/embed/18eJtrma3zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/18eJtrma3zk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

