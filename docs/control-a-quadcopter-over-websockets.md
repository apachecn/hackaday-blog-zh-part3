# 通过 Websockets 控制四轴飞行器

> 原文：<https://hackaday.com/2017/12/23/control-a-quadcopter-over-websockets/>

![](img/77db0ff01105b592d7acbdad61773740.png)

The interface

每个人都喜欢的 IOT 模块 ESP8266 通常是任何需要快速、廉价控制网络的项目的首选。[Andi23456] [想用他的豪华手机](http://www.instructables.com/id/Wifi-PPM-no-App-Needed/)控制他的四轴飞行器，并认为将一个 ESP12-E 模块永久绑定到四轴飞行器正是他所需要的。

ESP8266 真正展示了它的全面实力，它既托管了基于 HTML5 的操纵杆的 web 服务器，也托管了 Websockets 服务器，以便手机等客户端可以通过快速、低延迟的连接与之交互。一旦 ESP8266 接收到输入，它就使用中断来产生相应的 PPM(普勒位置调制)码，四轴飞行器上的 RC 接收器可以理解该码。非常酷！

真正使这种实时(ish)控制可行的是 Websockets，这种协议基本上允许您通过“升级”的 HTTP 连接灵活地交换数据，而不必在每次通信时都带着头。如果你没有听说过 Websockets，你真的应该看看这个库，看看这个视频，看看你能实现什么。