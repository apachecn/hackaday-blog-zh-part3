# 迷你间谍 Bug 演练

> 原文：<https://hackaday.com/2018/02/09/mini-spy-bug-walkthrough/>

我们最喜欢[GreatScott 的]项目视频的地方在于，他不仅展示了它们的制作过程，还展示了选择零件的计算过程以及过程中的修改。这一次，他制作了一个可以记录长达九个小时音频的迷你窃听器。

他的第一项任务是确定 ATmega328p 的 ADC 是否适合音频采样，但前提是他要通过定期检查麦克风的输入电压来解释采样的工作原理。查看数据手册，他发现 ADC 的最快转换时间为 13 微秒，相当于 76.923 kHz 的采样速率。够好了。

然后，他讲述了为什么以及如何决定使用基于 MAX9814 IC 的预制放大器电路。剧透警报。他的驻极体的放大器输出电压太低，使用现成的电路，而不是让他自己保持的东西简单，电路有自动增益控制。

此时，他添加了 MicroSD 卡适配器。为什么不像其他人一样通过调频传输音频呢？也许他担心有人检测到传输，然后[发现他的 bug](https://hackaday.com/2015/12/08/theremins-bug/) 。

他的最终优化包括获得良好的电池寿命。他测量出电路的电流消耗为 20 毫安。使用 160 mAh 的电池容量，可以录制 8 小时。移除 Arduino Pro Mini 的电压调节器和两个 led 使电流降至 18 毫安，记录时间为 9 小时。好多了。

那些是亮点。在下面的视频中欣赏他的完整演示。

 [https://www.youtube.com/embed/7Hn4UFi9wvs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7Hn4UFi9wvs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

