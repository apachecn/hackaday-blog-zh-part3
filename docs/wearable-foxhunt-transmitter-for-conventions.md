# 用于会议的可穿戴 Foxhunt 发射机

> 原文：<https://hackaday.com/2017/08/31/wearable-foxhunt-transmitter-for-conventions/>

业余无线电操作员[KE4FOX]想要建造自己的 2M[猎狐发射机](http://www.ke4fox.net/2015/08/14/2m-foxhunt-transmitter/)用于会议。它将被装在一个 1020 的鹈鹕微型盒子里，系在一个人身上，这个人会走来走去发送信号，让火腿去追踪狐狸。该项目使用插入低通滤波器的 DRA818 VHF/UHF 收发器，结合硬件 DTMF 解码器，所有这些都由 ATmega328P 控制，由 11.2 mAh 电池供电。

[KE4FOX]还蚀刻了自己的 PCB，使用 PCB 墨粉转印法，在电路板周围折叠一张转印纸，使两层对齐。然后他用氯化铜蚀刻电路板。组装电路板时，他意识到自己犯了一个严重的错误，以为收发器模块的引脚在顶层，而实际上它们应该在底层。他通过倒置焊接模块解决了这个问题。

他把这个项目放到 1020 中，安装了一个 SMA 天线。在他完成这个项目后，他发现他在 Arduino 的 5 V 数据上使用的电平移位器没有像预期的那样工作，而是停留在一个单一的频率上。为 V2 工作的东西！

我们在 Hackaday 上发布了大量业余无线电帖子，包括[用树莓皮猎狐](http://hackaday.com/2014/11/06/fox-hunting-with-a-raspberry-pi/)以及如何制作 [TDOA 定向天线](http://hackaday.com/2014/03/04/tdoa-time-difference-of-arrival-directional-antenna/)。

【谢了，那个 Kat！]