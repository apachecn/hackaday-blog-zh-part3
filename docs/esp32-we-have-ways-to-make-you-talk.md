# ESP32，我们有办法让你说话

> 原文：<https://hackaday.com/2018/02/06/esp32-we-have-ways-to-make-you-talk/>

《詹姆斯·邦德》系列电影中我们最喜欢的场景之一是[金手指]和[邦德]之间的经典对话。[康纳利](真正的邦德)说，“你希望我说话？”回答是，“不，邦德先生，我希望你去死！”不过，说到 ESP32，显然[XTronical]希望它能说话。他发布了一个库来简化在 ESP32 上播放 WAV 文件。还有一个视频值得一看，下面。

实际上，你可能想回到他以前的帖子，他[通过电路板上的一个数模转换器连接一个扬声器](http://www.xtronical.com/basics/audio/dacs-on-esp32/)。在那篇文章中，他只是推出了几个简单的波形，但硬件是他用来播放 WAV 文件的相同设置。

通过将 WAV 代码包装在一个库中，[XTronical]使得实际回放变得简单。下面是他的简单例子的核心:

```

void loop() {
static uint32_t i=0; // simple counter to output
if(ForceWithYou.Completed) // if completed playing, play again
    DacAudio.PlayWav(&amp;amp;ForceWithYou); // play the wav (pass the wav class object created at top of code
    Serial.println(i); // print out the value of i
    i++; // increment the value of i
}

```

不是很难，但是，当然，重物隐藏在两个物体`PlayWav`和`ForceWithYou`中。该视频解释了如何添加更多内容，但你也可以猜测。简而言之，他使用 Audacity 准备 WAV 文件，然后使用十六进制编辑器将字节放入数组。由于我们中的许多人使用 Linux 或 Cygwin，我们可能会尝试使用 od 或 hexdump，但是无论您如何做，它都必须以数组结束。

如果你想在波形产生方面做更多的实验，，[埃利奥特·威廉姆斯]在这方面做得很好。你也可能从我们的[信号发生器](https://hackaday.com/2015/09/15/how-to-build-a-pocket-sized-mbed-signal-generator/)中得到一些想法。

 [https://www.youtube.com/embed/gxpHDUHcBMk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gxpHDUHcBMk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

