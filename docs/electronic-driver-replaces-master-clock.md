# 电子驱动器取代主时钟

> 原文：<https://hackaday.com/2016/05/15/electronic-driver-replaces-master-clock/>

在廉价微处理器和通过 NTP 或从 MSF、WWVB 或 DCF77 等容易获得精确计时的时代，确保任何数量的时钟保持相同的时间都不成问题。在更简单的时代，虽然他们没有这些工具，所以当一个大型组织希望确保其所有部分同时运行时，他们使用机电解决方案。当时的钟表匠所能制造的最高质量的主钟装有微型开关。开关会向有螺线管的从属时钟发送脉冲，而传统的时钟有钟摆。因此，系统中的每一个时钟都以同样的速度失去或获得时间。

【Edo Lelic】有一个相当不错的伊斯克拉奴隶钟，可惜不是曾经驾驭它的主人。[没有被这个挫折吓倒，他创造了一个电子驱动板，可以产生所需的 100 毫秒脉冲](http://www.elektronika.ba/862/master-clock-driver-for-antique-slave-clocks/)。他选择的武器是 PIC 微控制器和 H 桥驱动器，以提供所需的电压和极性。该时钟被设计为接受 100V 脉冲，但由于它有一个内部串联电阻，他确定螺线管只需 24V 就可以了。源代码可以从链接文章的底部下载。

这些时钟是一种看不见的技术，在我们没有注意到的情况下正在消失。如果你找到一个，或者更好的是找到一个主时钟，你会发现它确实是一个非常高质量的时钟。主时钟非常值得抢购。至少现在你不用为它找太远的司机了。

我们在 Hackaday 还没有看到太多这样的项目。除了一个相当不错的数字主时钟外，这是一个未知的领域。或许，这也是[成为一个复古作品](https://hackaday.com/category/hackaday-columns/retrotechtacular-hackaday-columns/)的理由。

感谢[Muris puci]的提示。