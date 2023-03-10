# 黑客日奖参赛作品:绕过电视广播限制

> 原文：<https://hackaday.com/2016/09/28/hackaday-prize-entry-bypassing-tv-broadcasting-restrictions/>

这是电视观众面临的一个普遍问题，他们想看的节目正在播出，但没有送到他们的位置。电视内容传统上是按地理位置授权传输的，这有时会让观众与广播公司产生分歧。

观众并不总是接受这种对他们节目选择的限制，而是采用了各种具有不同程度的合法性和成功的创造性解决方案。许多年前，你可能会看到超长超高频天线捕捉遥远的发射机，最近这些努力已经在数字领域。据说在 20 世纪 90 年代，天空电视台的 Videocrypt 卫星电视智能卡被破解，例如，因为德国的《星际迷航》下一代粉丝无法购买非英国地址的订阅。你可以在评论中争论【帕特里克·斯图尔特】*等人*间接导致解密政变是否是一个都市传说，但不可否认的是，串行智能卡仿真器和用于天空解密的可疑 DOS 软件当时在整个欧洲都有销售。

现代打破电视广播地理壁垒的努力转向了互联网。命运多舛的 Aereo 和 Slingbox 机顶盒流媒体产品等服务将特定地区的电视广播转移到其他地方进行在线观看。但它们并不是唯一的互联网自我流媒体选项，如果付费订阅或捆绑商业服务的想法不具吸引力，那么你可以为自己建立一个停播流媒体。

[螺线管]的项目是[一个使用带有 USB DVB-T 调谐器](https://hackaday.io/project/10821-bypassing-tv-broadcasting-restrictions)的 Raspberry Pi 3 的停播流媒体工具。它使用 [Tvheadend](https://tvheadend.org/) 来驱动流媒体，使用 [OpenVPN](https://openvpn.net/) 来提供安全性。他的构建日志详细描述了他为确保功耗不太高以及 Pi 运行不过热所做的努力，并提供了如何设置和使用该软件的说明。它不是一个过于复杂的硬件，但它可以为任何希望在外出旅行时保持家庭电视更新的人提供有用的服务。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)