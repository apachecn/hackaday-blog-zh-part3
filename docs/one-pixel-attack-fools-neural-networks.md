# 单像素攻击愚弄了神经网络

> 原文：<https://hackaday.com/2018/04/15/one-pixel-attack-fools-neural-networks/>

深度神经网络可以很好地识别图像——几乎与吸引硅谷风险投资一样好。但它们也可能相当脆弱，过去几年的一系列研究项目一直致力于减少网络图像分类被故意愚弄的可能性。

一种特殊的攻击方式是向图像中添加特制的噪声，翻转网络黑暗深处的一些比特，使其看到其他人不会注意到的差异。我们得到了一个关于单像素攻击的 YouTube 视频提示，嵌入在下面，改变图像中的一个像素就可以欺骗网络。带上那个机器人霸主！

[![](img/608b539dc646a60eff2929bf74986d6c.png)](https://hackaday.com/wp-content/uploads/2018/04/dog_image.png)

We can’t tell what these are either..

或者没这么快。阅读[引用的论文](https://arxiv.org/abs/1710.08864)中的附属细则为深度神经网络描绘了一幅明显不那么悲观的画面。首先，问题中的图像一开始是 32 像素乘 32 像素，所以每个像素都很重要，尤其是在它通过几个像素窗口的卷积步骤之后。他们攻击的网络也不是最锋利的工具，大约有 68%的分类成功率。这意味着，对于许多测试图像来说，网络不确定从哪里开始——让它从勉强最好(正确)的第一选择翻转到第二选择应该不是很难。

这并不是说这一系列的研究，网络对抗训练，是假的。让神经网络对微小变化具有鲁棒性的想法很重要。举例来说，你不希望海龟被错误地归类为枪支，或者 Hackaday 自己的史蒂文·杜弗兰[被错误地归类为烟草商](https://hackaday.com/2017/06/14/diy-raspberry-neural-network-sees-all-recognizes-some/)。你肯定不希望语音识别软件被精心制作的背景噪音愚弄[。但是，如果 YouTube 上声称的“惊人的结果”看起来好得不像是真的，那么，也许它就是真的。](https://hackaday.com/2018/01/15/fooling-speech-recognition-with-hidden-voice-commands/)

感谢[kamathin]的提示！

 [https://www.youtube.com/embed/SA4YEAWVpbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SA4YEAWVpbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

