# 旧调制解调器，新互联网。

> 原文：<https://hackaday.com/2018/02/26/old-modem-new-internet/>

你还记得拨号调制解调器连接互联网时发出的刺耳声音吗？你怀念吗？可能不会，但[Erick Truter]——受一个论坛帖子和后来的一些建议的启发——用无处不在的 [Raspberry Pi Zero](https://www.youtube.com/watch?v=dsHNjxWzz-g) 将一个经典的调制解调器变成了 3G Wi-Fi 热点。

找到一个旧的 USRobotics USB 调制解调器——据称处于“工作”状态——他开始剥离调制解调器板的许多组件，为新的电子元件腾出空间。[Truter]发现对他来说，Raspberry Pi Zero W 难以维持可靠的网络，因此配备了标准 Pi Zero 和 USB Wi-Fi 加密狗。他还拆除了一个 USB 集线器，以弥补 Zero 的单一端口。现在，为了 21 世纪，更好、更快地重建调制解调器。

他能够——有些困难——轻敲原来的发光二极管作为启动状态显示器；此外，发射和接收 LED 根据流量闪烁，处理的数据越多，LED 就越亮。事实证明，设置 Wi-Fi 热点比预期的要容易——添加 3G 加密狗及其功能也是如此。添加声音几乎太多了——没有足够的空间来安装 USB 声卡。相反，[Truter]快速制作了一个小电路板，通过 GPIO 引脚传输音频，然后连接到扬声器——足以模拟调制解调器的女妖尖叫。

同样，我们最近推出了一款比看上去更有价值的计算器。

[Via[/r/RASPBERRY _ PI _ PROJECTS](https://www.reddit.com/r/RASPBERRY_PI_PROJECTS/comments/7z9hdz/hi_all_just_wanted_to_share_my_project_of_turning/)