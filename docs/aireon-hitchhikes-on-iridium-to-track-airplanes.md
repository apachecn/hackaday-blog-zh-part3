# 艾伦搭乘铱星追踪飞机

> 原文：<https://hackaday.com/2017/12/27/aireon-hitchhikes-on-iridium-to-track-airplanes/>

SpaceX 刚刚通过发射 10 颗铱星 NEXT 卫星结束了 2017 年。发射的一个注脚是每颗卫星上的“有效载荷”:一个来自“航空公司”的小设备箱。他们将实时跟踪世界各地的每一架飞机，这在技术上是可能的，但直到现在还没有人声称他们可以经济地做到这一点。

挑战一:避免增加飞机成本。Aireon 没有使用昂贵的卫星通信或增加专用设备，而是收听作为国际空中交通管制现代化的一部分已经安装的 ADS-B 设备。但是由于 ADS-B 是为飞机对飞机和飞机对地面设计的，所以 Aireon 有一些挑战需要克服。事实上，ADS-B 天线通常安装在飞机的腹部，阻碍了卫星的直接路径。

挑战二:到处听广告-B，少花钱。今天，当飞机在陆地上空飞行时，我们可以跟踪它们，但是在海洋中间，除了可能的其他飞机之外，在范围内没有接收器。Aireon 需要大量低轨道卫星来确保无论你在哪里都在覆盖范围内。搭载在铱星上给了他们覆盖范围，而成本只是建造他们自己卫星的一小部分。

这些铱星发射还创造了精确地球，一种通过 T2 的 AIS 广播跟踪船只的海上机器人。剩余的铱星 NEXT 卫星以及这些监听节点将于明年发射，以完成该网络。希望类似[马航 370](https://en.wikipedia.org/wiki/Malaysia_Airlines_Flight_370) 的神秘事件不会再次发生。

你不需要卫星网络来凑热闹。你可以在你所在的地方收听这些数据信号。我们有接收飞机发送的 ADS-B 的[指南，和接收船舶发送的 AIS](https://hackaday.com/2014/01/16/build-a-cheap-airplane-ads-b-radio-receiving-tracking-station/) 的[指南。](https://hackaday.com/2013/05/06/tracking-ships-using-software-defined-radio-sdr/)