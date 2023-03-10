# Hackaday 奖参赛作品:老年人自主跌倒检测

> 原文：<https://hackaday.com/2017/09/04/hackaday-prize-entry-elderly-autonomous-fall-detection/>

为了他的 Hackaday 奖参赛作品，[having11]正在制作一个简单廉价的跌倒检测通知按钮，老年人、小孩或其他受医疗条件影响的人都可以佩戴。根据疾病控制和预防中心提供的数据，我们做了一些事实调查，跌倒似乎是老年人受伤的主要原因之一(T2)。

该设备将感应跌倒，并向接受者的护理人员、爱人或朋友发送短信或电子邮件。也可以使用按钮手动触发通知。在它真正发送警报之前有 5 秒钟的延迟，允许取消错误的触发。收到警报后，接收者可以决定如何处理，以及情况是否需要呼叫紧急服务。

该设备使用 ESP8266、MPU6050 MEMS 陀螺仪-加速度计组合和 MyDevices [Cayenne 物联网服务](https://mydevices.com/)。Cayenne 物联网服务目前在 T2 对制造商和非商业用户免费。唯一需要的其他组件是一些分立器件和一个小的 LiPo 电池，使设备的成本低于 10 美元。整个组件装在一个 3D 打印的外壳中。下一步可能是使它更紧凑，并设计一个可以作为手臂或胸带或腰带佩戴的外壳。这种监控设备的一个重要要求是能够在它不能满足其主要要求时/之前发出通知。为此，也许添加低电量电池和低 WiFi 信号强度指示器会很好。

如果你有更多的改进建议，请在下面留言。

 [https://www.youtube.com/embed/sxtmIG4RKY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sxtmIG4RKY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



The [HackadayPrize2017](https://hackaday.io/prize) is Sponsored by:[![Digi-Key](img/451cc9c9dd3307f9cc00715f8e9632e5.png)](https://hackaday.io/digikey) [![Supplyframe](img/acce516476edc2011f11f70c89a4a2f6.png)](https://supplyframe.com/) [![Microchip](img/058307fc153f1ab19d84443be4f08cfb.png)](https://hackaday.io/microchip) [![Texas Instruments](img/3734f1c96ffff85ea2a7eaddc92844ba.png)](https://hackaday.io/ti)