# 手腕骨折？推特启用石膏模型

> 原文：<https://hackaday.com/2015/12/31/break-your-wrist-twitter-enable-that-plaster-cast/>

石膏模型是供朋友和家人张贴康复信息的空白画布。但是如果是假日季节，就需要给它们装上闪亮的 LED 灯。当[露西·罗杰斯医生]弄伤她的手时，她在她的石膏上放了一个能发推特的 led 圣诞树。

硬件非常简单——一些 RGB LEDs、一个 Arduino、一个蓝牙模块和一块电池。发光二极管和电线组成了圣诞树，所有的部分都用 Velcro 固定在石膏模型上。这使得电子设备可以在未来的 x 光扫描中被移除。有趣的部分是将 led 连接到 [#CheerLights 项目](http://cheerlights.com/about/)。CheerLights 是一个“物联网”项目，允许世界各地的人们的灯光同步到一条推文中设置的一种颜色。为了对 Arduino 进行编程，她使用了由[James Macfarlane] 编写的[代码，该代码允许将 LED 颜色设置为蓝牙 UART 数据中看到的任何 Cheerlights 颜色。](https://github.com/mcflan/cheerlights)

连接使用 MQTT 来协调，MQTT 是一种轻量级标准，在连接的设备中很流行。通过将 MQTT feed 连接到来自[Andy Stanford-Clark's] MQTT feed 的 cheerlights 主题(mqtt://iot.eclipse.org，主题为 cheerlights)，灯会对 Tweet 做出响应(Tweet #cheerlights 和一种颜色)。LED 颜色也可以通过电话从控制器中的颜色选择器工具中选择，或者直接通过 UART 选择。如果蓝牙连接断开，指示灯会随机改变颜色。显然，当她带着带 Twitter 功能的 led 闪光灯石膏手臂去参加会议时，代表们玩得很开心。除非你和别人分享你的成就，否则就没那么有趣了！