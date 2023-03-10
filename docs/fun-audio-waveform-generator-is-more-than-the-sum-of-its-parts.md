# 有趣的音频波形发生器不仅仅是其部件的总和

> 原文：<https://hackaday.com/2016/08/10/fun-audio-waveform-generator-is-more-than-the-sum-of-its-parts/>

[Joekutz]想要重建他在 [Instructables](http://www.instructables.com/id/Arduino-Waveform-Generator/) 上找到的[音频速率函数发生器项目](https://hackaday.io/project/12756-a-feature-rich-arduino-waveform-generator)。这个项目本身非常简单:它是一个 8 位电阻梯形 DAC，一个漂亮的外壳，其余的是固件。

[Joekutz]认为这还不够。他需要一个液晶显示器、一个扬声器和 1 赫兹的精度。单单液晶显示器就是一个疯狂的黑客。他对计算器进行逆向工程，只是为了使用显示器。但是，他没有在计算器上映射每个键并直接键入每个数字，而是只敲击四个 1、+、=和清除键。然后，他可以通过输入正确数量的 1 并将它们相加来输入任意数字。345 = 111 + 111 + 111 + 11 + 1.在他的视频中，他把这描述为一个“相当愚蠢”的想法。我们觉得很搞笑。

不过，该项目的核心是基于 Arduino 的波形发生器。在下面的第二个视频中，[joekutz]详细介绍了固件。如果您想了解 DDS 的简单介绍，请查看(或者阅读我们的更深入版本)。

他还为他的电位计定制了定位器，这样他就可以输入精确的数值。这些由特殊的旋钮和弹簧夹组成，它们一起工作，将一个普通的锅变成一个粗略的 8 路(或其他)开关。非常酷。

因此，即使您不需要基于 R-2R DAC 的波形发生器，也可以去看看这个项目。处处都有好主意。

 [https://www.youtube.com/embed/T9alyB4fznw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T9alyB4fznw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) 
 [https://www.youtube.com/embed/l5-peWe6Zt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l5-peWe6Zt4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

