# 广告之后，你的音频将会回来

> 原文：<https://hackaday.com/2018/02/13/your-audio-will-be-back-right-after-this-commercial-break/>

[LittleTern]对重复的广告感到厌烦，希望能够在每个商业广告时段将他们的卫星电视静音。试图破解他们卫星盒的红外协议没有成功，所以他们想——为什么不干脆把电视静音呢？

简单地考虑了一下为该功能单独配备一个遥控器的想法，[LittleTern]很快就放弃了这个选项，就像人们倾向于失去一个额外的遥控器一样。相反，他们使用索尼 Bravia 遥控器上的备用 RGYB 按钮——减少了全部遥控器，同时仍然控制红外静音系统。四个彩色按钮中的每一个通常不会做太多事情，所以它们被设置为不同的静音时间长度——为频道或一天中的时间定制。将代码发送到电视的系统是 Arduino Pro Mini，它控制红外 LED 和接收器，状态 LED 设置为根据按下的按钮发光。

有了[Ken Shirriff]对红外遥控器的研究中的有用文件——是的，[](https://hackaday.com/2016/02/23/555-teardown-and-analysis/)*[[Ken](https://hackaday.com/2017/07/14/worlds-worst-bitcoin-mining-rig/)[Schirriff](https://hackaday.com/2016/12/31/8008-exposed/)——[little tern]手里有了他们电视所需的代码和一个编程好的准备好的 Arduino。他们能够 3D 打印项目盒，将其连接到电视的红外接收器附近，并通过 USB 供电！奖金！*

 *[LittleTern]在博客中提供了他们的代码。有一个小的时间修补需要做，以确保它与给定的设置顺利工作，但否则，一去不复返的日子摸索遥控器，因为你的程序恢复！*