# 机器音乐阅读

> 原文：<https://hackaday.com/2017/05/25/taming-those-music-reading-demons/>

“该死的吉姆，我是黑客，不是音乐家！”套用原版《星际迷航》系列中麦科伊~~斯科蒂~~的话。嗯，我们中的一些人也是音乐家，一些人，像我一样，也是业余音乐家，还有一些人不知道高音谱号的整个音符。但是时不时地，你想要的音乐是活页乐谱的形式，你需要把它转换成你的黑客可以演奏的东西。如果你幸运的话，你可以找到一个软件，它会为你读取乐谱并输出一个 MIDI 或 WAV 文件。或者，就像我的手摇音乐播放器一样，你可能需要自己阅读足够的音乐，才能将音符转换成类似 555 定时器芯片的频率。我们将在这里深入研究这两种情况。

如果你看不懂乐谱，那么你应该仍然能够理解我们所说的要点。但是为了防止你感到困惑，我们在本文末尾加入了[一个非常快速的介绍](#readingMusic)。

## 光学音乐识别(OMR)

![MusicXML note example](img/0ed99ec75c12adb3d349d88877f8fbdb.png)

MusicXML note example

你可能听说过光学字符识别软件 OCR，它可以将纸上的文字转换成数字形式。还有音乐 OCR，或者更准确地说是 OMR，光学音乐识别软件。你将相机对准一页乐谱捕捉图像，或者给软件一个包含乐谱的图像文件或 PDF，它会将图像文件或 PDF 转换为你按下按钮就能听到的音乐，或者保存为 MIDI 或 WAV 文件，以便从其他地方播放。

为了试用，我找到了一款名为 [SharpEye 2.68](http://www.music-scanning.com/) 的高质量产品，有 30 天的免费试用期。它可以将音乐保存为 MIDI 文件， [MusicXML](https://en.wikipedia.org/wiki/MusicXML) ，以及 [NIFF](https://en.wikipedia.org/wiki/Notation_Interchange_File_Format) 格式。此处显示的 MusicXML 片段属于音符 A，是一个四分音符。正如你将看到的，SharpEye 做了一个令人印象深刻的工作，给出了一个干净的黑白图像。它还提供了必要的编辑工具来修复任何识别错误。

![Greensleeves captured in sunlight and in SharpEye](img/5c2e40abd913e80cff80ddaf9e071472.png)

Greensleeves captured in sunlight and in SharpEye

在我的第一次测试中，我在阳光下拍摄了歌曲《绿袖子》中第一行的照片。然后我把照片放入 GIMP，这样我就可以把它转换成 TIFF 文件，因为 SparpEye 只能读取 BMP 和 TIFF 文件。但是我没有增强。然后，我在 SharpEye 中打开图像，并告诉它“读取图像”。这是光学音乐识别步骤。最终的结果就是你在这里看到的快照，完美无瑕，只有相关的音乐。在快照中，我点击了其中一个音符，红色的，以显示这是可编辑的音乐，而不仅仅是静态图像。点击播放按钮，它播放完美。

我把它存成了 MIDI 文件。但是，MIDI 文件指定如何播放音乐以及音符，并且不包含音频本身。所以我用 [Anvil Studio](http://www.anvilstudio.com/) 把它转换成音轨，然后把音乐保存成 WAV 文件，你可以在下面听。对于任何想在 Anvil 中这样做的人，至少你可以做文件-打开歌曲和文件-导出混合音频。

<https://hackaday.com/wp-content/uploads/2017/05/greensleeves_sunlight.wav?_=1>

[https://hackaday.com/wp-content/uploads/2017/05/greensleeves_sunlight.wav](https://hackaday.com/wp-content/uploads/2017/05/greensleeves_sunlight.wav)![Captured bad music and in SharpEye](img/4036f6bda16db8e801ffa8231b36d391.png)

Captured bad music and in SharpEye

这些 OMR 程序需要清晰的音乐图像或 pdf 文件，以便更好地识别它们。例如，上面显示的例子在左边有一些阴影，这使得 SharpEye 无法阅读该部分。图像也聚焦不佳，这导致它在底部有很多错误。黄色背景的音乐是 SharpEye 在识别之前显示它是如何看到音乐的。

![The bad music after fixing](img/d2536194c53880a809ced84a082fe22a.png)

The bad music after fixing

像许多 OMR 程序一样，SharpEye 并不打算作为一个音乐符号工具。它不会为您定位音符，也不会在您添加谱号时调整它们的位置。然而，它确实给了你足够的编辑工具来纠正识别错误，这就是我所做的，添加回阴影区域，以及在底部添加它错过的笔记。我还插入了 3/4 拍号，因为这是一张乐谱中间的图像，所以不是原始的。有了这些修正，听起来刚刚好。

<https://hackaday.com/wp-content/uploads/2017/05/bad_music_fixed.wav?_=2>

[https://hackaday.com/wp-content/uploads/2017/05/bad_music_fixed.wav](https://hackaday.com/wp-content/uploads/2017/05/bad_music_fixed.wav)

在这一点上，你可以把它保存为一个 MIDI 文件，然后把它转换成一个 WAV 或 MP3，并把它传输到你的黑客。或者，如果你想进一步完善音乐，将它保存为一个 MusicXML 文件，并将其加载到你最喜欢的音乐符号软件中，例如 [Sibelius](http://www.avid.com/sibelius) ，以便进一步编辑。

### 图像预处理实验

我用平板扫描仪将歌曲《斯卡伯勒集市》(Scarborough Fair)的一整页扫描成 PDF 文件，这次包括歌词。由于 SharpEye 不读取 PDF 文件，我首先将它加载到 GIMP 中，并保存为 TIFF 文件。SharpEye 读起来有问题，所以我回到 GIMP，把它保存为高质量的 JPG，加载回 GIMP，导出为 TIFF 文件。出于某种未知的原因，沙佩耶能读懂那本书。

即便如此，识别效果还是很差，漏掉了大部分音乐。我怀疑这是因为音乐是白底灰调。我用 GIMP 中的色阶工具将它转换成白底黑字，这次识别效果更好了。

![Scarborough Fair in SharpEye](img/9411783bd3488f6c45e2d0b388c24348.png)

Scarborough Fair in SharpEye

在进行识别之前，我必须告诉 SharpEye，歌词可以在五线谱上面找到，因为默认情况下，它会在下面找到它们。在快照中，原始图像是带有黄色背景的音乐。如你所见，歌词中有一些错误，但文本是可编辑的。在快照中，我选择了“win”，这应该是“goin”。还要注意，识别出的音乐的线条是水平排列的，而不是垂直排列的，就像你在普通纸上看到的那样，就像它们在原始图像中一样。但是结果听起来还不错。

<https://hackaday.com/wp-content/uploads/2017/05/scarborough_fair_en.wav?_=3>

[https://hackaday.com/wp-content/uploads/2017/05/scarborough_fair_en.wav](https://hackaday.com/wp-content/uploads/2017/05/scarborough_fair_en.wav)

你可以在维基百科上找到其他光学音乐识别程序[的列表，](https://en.wikipedia.org/wiki/Optical_music_recognition) [SmartScore](http://www.musitek.com/) 是以某种形式存在时间最长的程序，始于 1991 年。还有一个 SharpEye SDK，从列表中可以看出，它被一些不同的产品使用。你甚至可以在 YouTube 上找到适用于 iPads、iPhones 和 Android 手机的应用程序演示。搜索“音乐扫描仪”似乎能找到一些好的和不好的。

## 将音符转换为频率

如果你面前有乐谱，而你的黑客是一个把单个音符直接转换成合适的声音的人，那该怎么办？WAV 和 MP3 文件无法工作，因为它们包含已经转换的音乐。

![Musical note frequencies and 555 timer circuit](img/bbe7b4257216077e8567305fafdba908.png)

Musical note frequencies and 555 timer circuit

做这件事的方法真的很简单。每个音符[都有相应的频率](http://www.phy.mtu.edu/~suits/notefreqs.html)。对于想要的音符，您的电路只需以该音符的频率循环扬声器。提供该频率的一种简单方法是在非稳态模式下使用 555 定时器电路，如图所示。在电路中，输出频率由电容 C、电阻 R1 和 R2 决定。通过查看 555 定时器输出的频率公式，可以清楚地看到这种依赖性。

![Resistances for musical notes and 555 timer circuit](img/1ed9c70b7213256d4656aacbb6ea8702.png)

Resistances for musical notes and 555 timer circuit

处理该公式的一种典型方法是使用固定的 R2 值，然后针对每个所需频率增加不同的电阻，如修改后的电路所示。现在让我们插入一个[可变电阻](http://hackaday.com/2016/09/16/resistance-in-motion-everything-you-should-know-about-variable-resistors/) Rn。从图中可以看出，我们首先将 Rn 添加到频率公式中，然后重新安排公式来求解 Rn。将该公式输入电子表格，你就可以得出所需音符所需的电阻值。

![Hand cranked 555 timer music player](img/91d8fddd00d203d6c94113313d2a70ac.png)

Hand cranked 555 timer music player

这种电路的一个例子就是这个手摇音乐播放器。音符被编码成一圈纸上的孔。孔沿着纸的宽度的位置决定了 13 个可能的音符中的哪一个被演奏。孔的长度控制音符弹奏的时间长度。

![555 timer music player circuit](img/39f7d5665a92db7034afa30dd47d787f.png)

555 timer music player circuit

音乐播放器的电路图显示了相同的 555 定时器电路，但 Rn 由 13 个不同的电阻代替，电阻值使用 Rn 公式计算。然而，电路在任何时候都只使用一个电阻。这是怎么做到的？

这 13 个电阻中的每一个都焊接到 13 个铜板中的一个上。在每个铜板的顶部是一根铜线。纸在金属板和金属丝之间滑动。只有当电线和金属板之间的纸上有一个洞时，它们才会产生电接触。这将相应的电阻引入电路，555 输出所需音符的正确频率。在图中，如果 D3 的电线和铜板之间有一个孔，我们将突出显示电路。

## 阅读音乐的快速入门

在我们结束这篇文章之前，这里是承诺的阅读乐谱的最小介绍，仅够理解这篇文章。

![How to read music for piano](img/1095f2154460d1d2517228c69f296309.png)

How to read music for piano

一个简单的开始方法是看钢琴上的琴键。每个键代表一个音符，用从 A 到 g 的字母表示。你总是可以找到 C，因为它是任何两个黑键组左边的白键。从 A 到 G 只有七个字母，但是仔细看键盘，你会发现黑白键的模式在每七个白键之后重复出现。

在称为乐谱的纸上，现代乐谱由一组称为五线谱的水平线组成(单数是五线谱或五线谱)。符号代表音符，符号的圆形部分放在一条线上或两条线之间。五线谱上符号的垂直位置告诉您它是哪个音符。哪个符号告诉你要保持音符多长时间。

还有更多的内容，但现在你可以阅读足够多的乐谱来理解这篇文章，至少可以在钢琴上敲对键。如果你想更深入了解，这份参考资料看起来不错。

## 尾注

我们在 Hackaday 上遇到过几次活页乐谱。[Dino]做了与我们讨论过的相同类型的音符到频率的转换，但是使用 Arduino 的 tone()函数为他的[新年前夜迷你落球机](http://hackaday.com/2011/12/30/build-your-own-mini-ball-drop-for-new-years-eve/)的扬声器播放它们。【祖尔科】[当他想演奏他在穿孔纸卷上找到的编码时，他就用 Python 和傅立叶变换器制作乐谱](http://hackaday.com/2014/04/12/transcribing-piano-rolls-with-python/)。

说到这里(呻吟)，你尝试过哪些音乐上的滑稽动作？你有没有在任何黑客中处理过乐谱？请在下面的评论中与我们分享。