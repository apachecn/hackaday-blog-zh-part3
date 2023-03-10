# Jean-Luc PYcARD 是一个便携式 Python 开发平台

> 原文：<https://hackaday.com/2017/02/23/jean-luc-pycard-is-a-pocketable-python-development-platform/>

一个可笑的双关语和棋盘底部让·卢克·皮卡德的[屏幕印](https://hackaday.io/project/19597-pycard-jean-luc-pythonarduino-in-card-shape)足以获得参加 [2017 年黑客日科幻大赛](https://hackaday.io/submissions/2017-sci-fi-contest/list)的资格，这是一件好事，因为【bobricius】的 Python-plus-Arduino 卡和环境传感器百花香非常酷。

PCB 设计本身就很棒。它有一个巨大的 LED 阵列，一个腕带的切口，和一个板载 USB 插头，所以你可以通过把它插在你的电脑上来编程；当你插入时，它显示为一个 USB 大容量存储设备。“驱动器”上显示的文件是 Micropython 代码，您可以编辑、保存，然后直接在设备上运行。为了方便起见，你几乎不能击败它。

还有一整套传感器:不是一个而是两个温度和湿度传感器，包括我们最近最喜欢的 BME280，它也可以读取气压。(我们怀疑这使它成为三重录音机。)有一个实时时钟，一个蜂鸣器，还有一些按钮。想要添加更多传感器？为了您的方便，I2C 港口被打破了。

除了拥有《星际迷航》的天赋之外，这个平台还会给各种教育平台带来机会: [Micro:bit](http://hackaday.com/2016/06/03/hands-on-with-the-bbc-microbit/) ，我们正看着你。确实非常酷！