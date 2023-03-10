# 聆听大地的声音

> 原文：<https://hackaday.com/2015/12/01/listening-to-the-sounds-of-the-earth/>

地震检波器是一种专门制造的麦克风，用来听地球的声音。[JTAdams]发现它们价格合理，所以[买了一些和](http://jtadams.ca/articles/14/geophone-sensors)一起玩。地震检波器用于检测来自地震、爆炸、隆隆卡车和可控震源车的振动。为了发挥作用，它需要一个放大器和一个记录设备来捕捉信号。

![24](img/18ab09b1c84b7c56e71a6a7221907dbb.png)

[JTAdams]使用 LT1677 运算放大器的标准放大器设计，将信号馈入 MCP3008 模数转换器，并使用 Raspberry Pi 读取输出。Python 脚本将数据记录到 CSV 文件中进行处理。Pi 工作得很好，因为整个设置需要可移植到现场。另一个 Python 脚本绘制了可从网页获得的数据。呈现原始数据的简洁方法。[JTAdams]承诺将来会提供更多关于数据后处理的信息。如果你自己建造了一个地震检波器，你就不需要它来探测地震波，但是一个真正的手机会更坚固。

哦，什么是可控震源？它是一辆卡车，下面有一个大平板。该板被液压降低到地面上，直到卡车的重量压在上面。然后卡车使板振动，通常从 10 赫兹到 100 赫兹。这种次声波穿过地面，直到被下面的岩层反射回来。一长串地震检波器，大概有 1000 英尺长，检测到这些波，并记录下来。实际上，许多卡车被用来产生足够强度的同步信号。或者，你可以引发爆炸，这是在水中使用的技术。通常，这些信息用于石油和天然气勘探。休息之后，一个卡车运行的视频。

 [https://www.youtube.com/embed/4El6U0XTNS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4El6U0XTNS0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

