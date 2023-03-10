# Hackaday 奖参赛作品:AutoFan 通过面部识别拯救疲惫的司机

> 原文：<https://hackaday.com/2016/09/17/hackaday-prize-entry-autofan-saves-tired-drivers-with-face-recognition/>

长途驾驶有时会很乏味。耀眼的阳光和你所有车窗的温室效应使它又热又干。你打开风扇，或者空调(如果有的话),就会感到轻松。很快你就有了另一个问题，干冷的空气让你的眼睛不舒服。最终，当你越来越累的时候，你会发现当你保持警觉的时候，你越来越需要脸上的空气。因此，你大部分时间都在摆弄通风口或调节气候控制。如果汽车能为你做所有这些，那不是很好吗？

AutoFan 是来自[hanno]的一个项目，[旨在智能地自动化这个过程](https://hackaday.io/project/12384-autofan-automated-control-of-air-flow)。它有一个带可控百叶窗的风扇，由一个带网络摄像头的 Raspberry Pi 2 驱动。Pi 计算驾驶员面部的位置，并确保来自风扇的空气被导向一侧。如果它发现司机的眨眼频率增加，它就会将空气导向他们的面部，因为它已经检测到他们开始疲劳了。

构建日志详细介绍了 OpenCV 中计算伺服角度和校正相机镜头失真的数学方法。他们还讨论了用于利用多核架构和控制伺服系统的 Python 代码。原型风扇住房可以在视频中看到下面的休息，完成了一个不为所动的猫。对于那些对代码感兴趣的人，他已经在 GitHub 库中提供了代码。

[https://player.vimeo.com/video/174260898](https://player.vimeo.com/video/174260898)

我们以前从未在 Hackaday 有过面部识别驱动的汽车气候控制。然而，我们已经将面部识别[用于衡量在线游戏玩家的情绪](http://hackaday.com/2012/04/04/facial-recognition-software-can-tell-when-youre-frustrated-with-xbox-live/)，尽管该项目依赖于在线服务的 API，而不是自己做工作。

The [HackadayPrize2016](https://hackaday.io/prize) is Sponsored by:[![Atmel](img/2e52aec37df7a9bb2e83735e78e154fe.png)](https://hackaday.io/atmel) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://www.digikey.com/) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/)