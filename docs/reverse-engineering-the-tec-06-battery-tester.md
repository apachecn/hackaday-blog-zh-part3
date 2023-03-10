# 对 TEC-06 电池测试仪进行逆向工程

> 原文：<https://hackaday.com/2018/01/22/reverse-engineering-the-tec-06-battery-tester/>

[Syonyk]了解到您可以将几根电线焊接到 TEC-06 电池容量测试仪上，将其连接到 TTL 串行适配器上，它将通过串行端口与一些 Windows 软件接口。您可以购买已经启用串行的版本，但由于他有非连接版本，他有兴趣尝试一下。不仅有效，他还花时间对协议进行逆向工程，并详细记录了他的发现以及他是如何解决这个问题的。

在这里，我们从来不需要借口来逆向工程任何东西。但是 Synonyk 提到他不喜欢使用中国的 Windows 专用软件。如果他想在 Linux 上使用它，或者如果新版本破坏了 Windows 兼容性，或者如果软件中有间谍软件，他希望能够继续使用该设备。当然，他也承认——我们明白——他也只是喜欢这样做。

他的第一步是找到 CPU 的数据表，并验证何频读到的看起来像是串行数据。的确是。然后，他用示波器验证串行数据是否出现。这意味着串行和非串行设备可能具有完全相同的固件，而非串行设备只是没有连接到端口的组件。

之后，他拿出了一个更好的示波器，一些基于 Windows 的串口嗅探软件，开始破解这个难题。一旦他对端口的配置有了概念，他就转向 Linux，在那里他发现设置一个非标准的波特率，比如 128，000 甚至奇偶校验，是多么痛苦。然后，他制定了协议，[编写了代码来推出一个包含数据](https://github.com/Syonyk/TEC06)的 CSV 文件。

这让我们想起了一个非常熟悉的家伙出于许多相同的原因入侵了 MHS-5200A 协议。有这么多来自中国的[电子产品被黑客攻击成这样](https://hackaday.com/2016/06/28/reverse-engineering-quadcopter-protocols/)，你几乎希望他们能帮我们省点麻烦，公布一下规格。话说回来，这有什么好玩的？