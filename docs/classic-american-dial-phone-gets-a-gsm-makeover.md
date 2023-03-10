# 经典的美国拨号电话得到 GSM 改造

> 原文：<https://hackaday.com/2018/04/18/classic-american-dial-phone-gets-a-gsm-makeover/>

对于坚定的功利主义者来说，很少有设计比西方电气 500 型台式电话更好。500 做了一件事，而且做得很好，从 20 世纪 40 年代中期到 70 年代初按键式电话开始出现，它基本上保持不变。然而，这并不意味着它不能在现代电话系统中占有一席之地，只要你愿意将它转换成手机。

对[bicapitate]来说幸运的是，一旦网络接口被移除，Model 500 在机箱内有足够的空间，因为新的电子设备占用了相当多的空间。没有构建日志*本身*，但是相册清楚地显示了正在发生的事情。Arduino 读取挂机开关和拨号脉冲，而 Fona GSM 模块负责蜂窝方面的事情。它看起来像一个小的驻极体麦克风和一个扬声器取代了原来的发射器和接收器。作为一个很好的接触，原来的 ringer 被使用，但不是试图用电来驱动它，[bicapitate]想出了一个简单的小马达上的凸轮机构。以正确的速度驱动，凸轮钩住铃锤臂，敲响一个铃，然后松开它，让铃锤弹回，击打另一个铃。一切都是由一个脂肪驱动的，所以它可以被带到当地的咖啡店去喝一些时髦的 hijinks。

在使用世界各地的手机之前，我们见过类似的复古模式；[这是英国的](https://hackaday.com/2017/09/28/classic-british-phone-gets-a-google-makeover/)和比利时的[的](https://hackaday.com/2015/11/18/old-school-rotary-phone-gets-gsm-upgrade/)，两者都使用同样经典线路的手机。

[通过 [r/arduino](https://www.reddit.com/r/arduino/comments/8bzqyf/i_converted_a_1961_western_electric_model_500/)