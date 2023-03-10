# 使用 Raspberry Pi 文本到语音转换

> 原文：<https://hackaday.com/2018/03/02/diy-text-to-speech-with-raspberry-pi/>

我们几乎可以指望我们的视力随着年龄的增长而衰退，甚至可能已经过了矫正的年龄。如果你问我们，这是一个相当大的缺陷。那么，一个眼睛老化的人如何希望继续阅读印刷的文字呢？

有很多商业文档阅读器可以将文本转换成语音，但是它们很贵。大多数需要智能手机和/或互联网连接。对于未来几代失明的人来说，这可能不是什么大问题，但我们还没有到那一步。与此同时，我们有小型廉价的电脑和大量的开源软件，可以把它们变成文档阅读器。

[rgrokett]建立了一个 RaspPi 文本阅读器来帮助年迈的父母保持他们的独立性。在这个过程中，[他为建造 one](https://www.instructables.com/id/PiTextReader-an-Easy-to-Use-Document-Reader-for-Im/) 做了一个很好的一应俱全的指南。使用起来再简单不过了——只需将文件放在摄像头下，然后按下按钮。Python 脚本让 Pi 给文本拍照。然后，它使用[的宇宙魔方 OCR](https://github.com/tesseract-ocr/tesseract) 将图像转换成纯文本，并通过[的语音合成引擎](http://www.festvox.org/flite/)将文本大声朗读出来。只要插上电源，阅读器就一直开着，所以只要按一下按钮，它就可以工作了。我们可能都很欣赏这样一个低争议的设计。请务必在休息后观看演示。

如果你想用这个看书，你还是得自己翻页。这里有一个 BrickPi 阅读器可以解决这个问题。

 [https://www.youtube.com/embed/n8-qULZp0Go?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/n8-qULZp0Go?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

