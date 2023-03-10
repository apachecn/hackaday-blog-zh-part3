# 具有 OCR 和文本到语音转换功能的移动文本阅读器

> 原文：<https://hackaday.com/2016/03/21/mobile-text-reader-with-ocr-and-text-to-speech/>

现在有一些设备可以使用漂亮的相机和显示器放大文本，还有一些设备可以将文本转换成盲文，文本到语音转换软件已经存在了三十年。为了参加我们的 Raspberry Pi Zero 竞赛，[Markus]决定将所有这些想法结合到一个简单的设备中[，该设备将把印刷文字转化为语音](https://hackaday.io/project/9669-texteye-raspberry-pi-zero-mobile-textreader)。

[Markus]项目的动力来自于一群失明的计算机科学学生。这些学生使用专门的程序，该程序使用专门的硬件和软件，如移动盲文终端、OCR 和口试，使这些学生能够像其他人一样学习相同的东西。[Markus]想要生产类似的东西，使用简单的文本到语音转换软件，而不是复杂的盲文显示器。

[Markus]项目的物理设计具有独特的功能——一个手持设备，前面有一个摄像头，中间有一个 Pi，后面有一个扬声器和耳机插孔。手柄包括一个大电池和一个触发器，用于告诉 Pi 大声朗读几个单词。

该软件是围绕 [SnapPicam](https://learn.adafruit.com/snappicam-raspberry-pi-camera) 构建的，包括许多已经需要的功能。有了[宇宙魔方](https://github.com/tesseract-ocr/tesseract)，OCR 在很大程度上是一个已解决的问题，而有了 [Festival](http://www.cstr.ed.ac.uk/projects/festival/) ，文本到语音转换变得很容易。

虽然[Markus]只是将一些现有的软件模块连接在一起，但他已经推出了一款独特的设备，对任何有视力障碍的人来说都非常有用。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看全部词条](https://hackaday.io/submissions/adafruitpizerocontest/list)