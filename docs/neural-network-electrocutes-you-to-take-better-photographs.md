# 神经网络让你拍出更好的照片

> 原文：<https://hackaday.com/2018/02/09/neural-network-electrocutes-you-to-take-better-photographs/>

拍一张糟糕的照片容易得可笑。你的大脑是一个比 Photoshop 好得多的 Photoshop，它对你的眼睛捕捉的场景所做的大量编辑经常导致你看到的和你拍摄的之间明显和令人失望的差异。

将你的大脑从摄影循环中解放出来是[Peter Buczkowski]的"[假肢摄影师](https://hackaday.io/project/47538-prosthetic-photographer)的目标这个想法是使用一个神经网络来不断地分析一个场景，直到达到最大的美学价值，这时用户会无意识地拍摄照片。

但是人机界面是有趣的一点——该设备使用经皮电神经刺激器(TENS)连接到手柄中的电极，以不由自主地收缩用户的手指肌肉并扣动扳机。(编者注:这个项目是尽可能科幻的——计算机大脑正在拉动肉傀儡的绳子。哇哦。)

同时，回到现实中，这并不是一个太奇怪的项目。树莓派通过 Pi 摄像头观察场景，并使用针对一组高质量照片训练的 TensorFlow 神经网络来确定何时按下快门。下面的视频展示了它的工作情况，[【Peter】的博客](http://www.peterbuczkowski.com/projects/prosthetic-photographer)上有一些用它拍的照片。

我们不确定这是否是下一个“必须拥有”的相机配件，它可能不会对快照和自拍有所帮助，但它是一个有趣的人机界面。如果你正在考虑相机内部的神经网络提示你何时拍照的可能性，你可能想看看我们关于 TensorFlow 的初级读本[来开始。](https://hackaday.com/2017/04/11/introduction-to-tensorflow/)

[https://player.vimeo.com/video/253938770](https://player.vimeo.com/video/253938770)

感谢[Peter]的同事[Julian]，他给我们提供了这个消息。