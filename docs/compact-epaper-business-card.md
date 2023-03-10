# 紧凑型电子名片

> 原文：<https://hackaday.com/2016/08/23/compact-epaper-business-card/>

你的名片是否华而不实？紧要关头有用吗？它们每个售价 32 美元，还配有电子纸显示屏吗？没有吗？好吧，那就尽情欣赏这张由[ 保罗·肖 ]制作的电子名片吧。为了保持忙碌并挑战自己，他开始制作一种可以每隔几个月更新一次的名片，而不是每当他更新信息时就购买一叠新的名片。

之前与 ePaper 合作过，这似乎是[Schow]实现其项目超低功耗标准的首选——最终决定采用 2 英寸显示屏。为了快速执行这个项目，他在 KiCad 中设计了电路板，经过几个小时的简化，简化为电源控制、40 引脚连接器和一些电阻和电容。在这种情况下，40 针连接器的不正确方向以及其他一些错误造成了匆忙的浪费。然而，2.0 版本是一个完美的概念验证，而 3.0 看起来更时尚、更专业。

[![Final 3.0 Card With Wrencher](img/d5c6955d10fa32d5729808cd0ff9b61b.png)](https://hackaday.com/wp-content/uploads/2016/08/final-3-0-card-with-wrencher.jpg)

[Schow]建议在焊接到如此小的电路板时使用放大镜或显微镜——幸运的是附近的 tinker mill——Longmont makers space 就有一个。他还因为电量不足而遇到了显示器变暗的问题，但通过添加一个 TLV61225DCKR 升压转换器解决了这个问题。当为了增加效果而改变图像时，背面的灯会闪烁。虽然这是一张独特的“实用性可选”的名片，但如果你在乎自己的钱包，就不要分发太多这样的名片。

对于其他很酷的电子名片，看看这张[大容量存储名片](http://hackaday.com/2012/10/04/limpkins-new-business-card/)——或者这张[紧急工具包卡！](http://hackaday.com/2013/12/02/an-engineers-emergency-business-card/)