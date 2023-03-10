# 黑掉 Raspberry Pi WiFi 天线以获得更多 DB

> 原文：<https://hackaday.com/2016/03/18/hacking-the-raspberry-pi-wifi-antenna-for-more-db/>

我一直在测试 Raspberry Pi 3，我发现的一件事是，这款新机型中添加的 WiFi 天线不是特别好:在其他设备没有问题的地方，Pi 连接到我的 WiFi 网络有问题。这并不奇怪，因为 Pi 3 上的天线很小:安装在显示器连接器旁边，只有几毫米宽。DorkbotPDX 的[Ward]同意这一点，所以他[决定通过增加一个外部连接器](http://www.dorkbotpdx.org/blog/wramsdell/external_antenna_modifications_for_the_raspberry_pi_3)来增加一个更好的天线。

他尝试了两种方法:用尾部连接器替换天线，并在电路板上未使用的焊盘上添加 U.FL 连接器。两者都需要一些精细的焊接工作，所以不能轻易接近。用外部连接器替换天线使信号输出显著增加，这应该等同于 WiFi 连接的更大范围。

有趣的是，Pi 3 的电路板上有焊盘，用于添加外部天线连接器，但没有使用。另外，其中一个焊盘被阻焊膜覆盖。使用这些是[Ward]使用的第二种方法，焊接一个 U.FL 连接器，并将其连接到一个小橡胶 duckie 天线。同样，这被证明更有效，大大增加了天线的功率输出。

注意:这个黑客肯定属于“不要在家里尝试这个”的范畴。摆弄天线会使 Pi 的保修和 FCC 认证失效，如果不小心的话，还会导致各种与信号相关的不愉快。