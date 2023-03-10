# 值得骄傲的 MIDI 音序器

> 原文：<https://hackaday.com/2018/06/23/a-midi-sequencer-to-be-proud-of/>

MIDI 音序器出奇的昂贵，这使得它们成为[RH Electronics]的一个极好的目标，他创造了一个十六步装置。它支持每个步骤多达八个可播放的部分，可以是 MIDI 或鼓触发器。

表壳和前面板是按照非常高的标准建造的，内部的一块条形板上有一个 ATmega644 负责所有的 MIDI 工作，一个 ATmega328 负责运行许多 led，还有一个 ATtiny85 负责读取前面板按钮。整体由 644 上的定时器保持同步，以产生所需的 MIDI 时钟。还有一个 LCD 显示器，它带有状态和编程界面。

你可以在休息时间下面的视频中看到结果，在这个视频中，音序器被测试，旁边是一个匹配的合成器的诱人一瞥。这是另一个项目，还是一个商业设备，当我们试图找到它时，谷歌却失败了？同时，这肯定不是我们在 Hackaday 为您带来的第一个 MIDI 音序器，[这个 Arduino one](https://hackaday.com/2013/02/22/arduino-controlled-midi-sequencer/) 是几个也使用 Atmel 器件的另一个例子。

 [https://www.youtube.com/embed/sm-y5gQlOpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sm-y5gQlOpI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

