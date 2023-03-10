# GPS 追踪器获得短信升级

> 原文：<https://hackaday.com/2017/07/06/gps-tracker-gets-sms-upgrade/>

2000 年 5 月，时任总统比尔·克林顿签署了一项指令，将为任何人提高 GPS 的精度。在这个开关被打开之前，这个能力只有军方才有。随之而来的是日常导航系统中最引人注目的 GPS 设备的冲击。市场上的大量新设备也将价格压低到几乎任何人都可以从头开始制造自己的 GPS 跟踪设备。

[Vadim]发明的 GPS 追踪器不仅使用 GPS，也使用 GSM 网络。他使用 Neoway M590 GSM 模块访问蜂窝网络和 NEO-6 GPS 模块。蜂窝网络用于发送 SMS 消息，详细说明单元本身的位置。一切都由 ATmega328P 控制，锂离子电池和一些电容器完善了完全集成的构建。

[Vadim]详细介绍了所有模块的工作原理，并逐步说明了它们的使用方法，远远超出了普通数据表中的内容。GSM 和 GPS 模块的配对似乎配合得很好，就像我们看到的 GPS 和 [APRS](https://en.wikipedia.org/wiki/Automatic_Packet_Reporting_System) 为了类似的目的而配对:[追踪气象气球](http://hackaday.com/2015/03/24/aprs-tracking-system-flies-your-balloons/)。