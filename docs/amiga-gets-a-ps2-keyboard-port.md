# Amiga 获得一个 PS/2 键盘端口

> 原文：<https://hackaday.com/2017/10/20/amiga-gets-a-ps2-keyboard-port/>

说出任何一台复古电脑——Apple II，Sinclair，甚至 TRS-80——你会发现一个社区深深地致力于让它保持活力。很难说哪个平台拥有最多狂热的粉丝，但我们猜测准将就在那里，阿米加的粉丝似乎特别投入。这就是这个 Amiga PS/2 鼠标端口的来源。

Amiga 是一种远远领先于其时代的机器，人们只是不了解它。在多媒体成为一种东西之前，它是一台真正的多媒体机器，能够很好地支持至今的声音和图像。从[jtsiomb]的工作站来看，他仍然在很好地使用他的 Amiga，尽管每次需要使用它时都要进行不方便的电缆交换。为了解决这个问题，[jtsiomb]开发了一个仿真器，可以将来自外部 PS/2 键盘的扫描码转换成 Amiga 键盘信号。仿真器嵌入在 Amiga 外壳中，可以拦截内部键盘连接器，仿真器是 ATmega168，它通过查找表进行强力转换。背面的开关允许他通过 KVM 开关选择内置键盘或 PS/2 键盘。

阿米加斯真的还有意义吗？截至两年前，[一家还在为一所学校](https://hackaday.com/2015/07/23/this-little-amiga-still-runs-school-districts-hvac/)运行暖通空调系统。我们不确定这是机器的证明，还是更多的官僚惰性，但无论如何，这都令人印象深刻。

[通过[遥控/电子](https://www.reddit.com/r/electronics/comments/76y5hl/i_made_a_ps2_keyboard_controllerconverter_to/)