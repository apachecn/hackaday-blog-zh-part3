# 借助音频 I/O 多路复用器逃离电缆地狱

> 原文：<https://hackaday.com/2015/11/02/escape-cable-hell-with-a-multi-io-audio-multiplexer/>

如果你曾经发现自己在音频输入和输出的混合之间切换，并且厌倦了总是插电缆，那么看看[winslomb]的带有集成放大器的[音频多路复用器。该设备可以接受四个音频输入中的任何一个，通过放大器传递信号，并将其发送到四个输出中的任何一个。](http://winslomb.blogspot.in/2015/10/audio-multiplexer-with-integrated.html)

音频放大器有一个音量控制，输入和输出可以通过按钮选择。Arduino Pro Mini 负责根据按钮按压来切换继电器。在输入端，您可以插入电话、电视、数字音频播放器或电脑等设备。输出可以馈入扬声器、耳机或耳塞。

在建筑的中心是一个 75 兆瓦的立体声音频功率放大器。这款音频运算放大器设计用于驱动 32 欧姆负载，因此当连接到低阻抗器件时，性能可能会受到影响，但对于耳机和小型电脑扬声器来说，它似乎工作正常。双组电位计控制音量，芯片具有有用的去爆音功能。该电路基本上是数据手册中所示基准电压源的翻版。输入或输出之间的切换由一组带有 MOSFET 输出的 [TLP172A 固态继电器](http://www.toshiba.com/taec/components/Generic/BCE0034_catalog.pdf)处理，并且所有这些都与微控制器联系在一起，允许以后添加 WiFi 或 BLE 功能。

[winslomb]使用 Eagle 布局设计，他在大电容和光继电器上犯了几个尺寸错误。(就像他说的，总是仔细检查脚印部分！)最后，他将它们焊接到电路板上，但它们可能会在下一次修订时修复。

[winslomb]在获得 EE 硕士学位的过程中，制造了这款交换机作为他的[顶点项目](http://edglossary.org/capstone-project/)，尽管这款设备的功能符合要求，但仍有改进的空间。 [GitHub 库](https://github.com/winslomb/Capstone)包含了所有的硬件和软件资源。请观看下面的视频，其中他演示了该设备的运行情况。如果你在寻找更简单的东西，这里有一个带 USB 控制的[两输入一输出音频切换器](http://hackaday.com/?s=audio+multiplexer)，在光谱的另一端，这里有一个连接到互联网的音频切换器[。](http://hackaday.com/2011/11/15/audio-output-selection-courtesy-of-the-internet/)

 [https://www.youtube.com/embed/jnQE9K1tzcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jnQE9K1tzcA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

