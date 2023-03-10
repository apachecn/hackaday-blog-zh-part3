# 用于您的合成器架的基本序列器

> 原文：<https://hackaday.com/2018/03/02/basic-sequencer-for-your-synth-rack/>

音序器对于给你的音乐带来规则的结构很有用，特别是如果你喜欢用架装式合成器。[【little-scale】在此分享一款 ADC 二进制门序列器，供您设置使用。](http://little-scale.blogspot.com.au/2018/02/adc-binary-gate-sequencer.html)

为了追求更大的极简主义，该建筑依赖于一个没有外部振荡器的准系统 ATMega328p。相反，使用芯片的内部 RC 振荡器。仍然可以在 Arduino IDE 中使用它，作为这里的[小规模]共享。

音乐制作从时钟输入信号开始，该信号是从 rack synth 的其他地方接入的。时序由电位计控制。有四个电位计和四个相应的输出通道。所有电位均由板载模数转换器读取，并将位置转换为 8 位值，范围为 0 至 255。我们最好的理解是，8 位数字随后被用作后续序列。例如，如果电位计设置为 255，即二进制的 11111111，序列器将在每一拍触发。相反，如果电位计转到最大值的 2/3 左右，ADC 读取值为 170，则二进制数为 10101010，每秒钟触发一次。

这是一种用最少的输入设备给几个通道排序的有趣方法。虽然它可能不是最直观的系统，但它确实适合机架安装狂热者津津乐道的旋钮和转盘。一定要看看下面的视频[小规模]的机架安装声音和令人印象深刻的漂亮录像。面包板从来没有这么好看过。

机架安装合成器新手？看看这个。

 [https://www.youtube.com/embed/xqWwSKXZuRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xqWwSKXZuRA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

