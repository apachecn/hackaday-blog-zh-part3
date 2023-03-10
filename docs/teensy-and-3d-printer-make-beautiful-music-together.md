# Teensy 和 3D 打印机一起创造美妙的音乐

> 原文：<https://hackaday.com/2017/04/29/teensy-and-3d-printer-make-beautiful-music-together/>

[Otermrelik]想要尝试 Teensy 音频库和适配器。这与他的 3D 打印机相结合，导致了一个非常酷的 [teensypolysynth](https://github.com/otem/teensypolysynth/) 的构建。该设备看起来像一个小迷你共鸣板，带有滑块和 3D 打印的旋钮。你可以在下面的视频中看到(听到)。

Teensy 音频库支持几个输出设备，包括几个内置选项和外部板，如这里使用的音频适配器。该库提供 CD 品质的声音，支持复音回放、录音、合成、混音等等。

[![](img/2ed42015396d245a58ef1ff97b15479f.png)](https://hackaday.com/wp-content/uploads/2017/04/td_libs_audio_gui.png) 更有趣的是，有一个音频设计工具可以在你的[网络浏览器](https://www.pjrc.com/teensy/gui/index.html)中运行，用于以图形方式构建代码的音频部分。尽管它在浏览器中，但它并不与服务器绑定，因此您可以离线运行该工具，而不必担心您改变世界的音频设计泄露到互联网上。浏览该工具是感受该库提供了多少功能的好方法。

该工具可以导出您添加到项目中的代码，如果您需要进行更改，还可以再次导入它。总的来说，很圆滑。当然，库完成了所有的工作，从这个简单的导出代码中可以看出:

```
#include <Audio.h>
#include <Wire.h>
#include <SPI.h>
#include <SD.h>
#include <SerialFlash.h>

// GUItool: begin automatically generated code
AudioSynthWaveform waveform1; //xy=344,303
AudioInputAnalog adc1; //xy=351,227
AudioMixer4 mixer1; //xy=485,230
AudioEffectFlange flange1; //xy=657,237
AudioFilterFIR fir1; //xy=804,233
AudioOutputAnalog dac1; //xy=947,227
AudioConnection patchCord1(waveform1, 0, mixer1, 3);
AudioConnection patchCord2(adc1, 0, mixer1, 0);
AudioConnection patchCord3(mixer1, flange1);
AudioConnection patchCord4(flange1, fir1);
AudioConnection patchCord5(fir1, dac1);
// GUItool: end automatically generated code
```

构建细节有点简单，但是在代码、图片和 [3D 可打印文件](https://www.thingiverse.com/thing:2041238)之间，你可能就能搞清楚了。你的布局可能会有一点不同，但无论如何你可能会想要的。

我们之前谈过 [Teensy 音频库](https://hackaday.com/2014/09/30/the-teensy-audio-library/)，我们仍然印象深刻。如果你不喜欢音乐合成，不要担心。你不能不喜欢[这个变声器](https://hackaday.com/2016/11/09/stormtrooper-voice-changer-helmet-uses-teensy-to-mangle-audio/)。

 [https://www.youtube.com/embed/KbcNqarBTsI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KbcNqarBTsI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

