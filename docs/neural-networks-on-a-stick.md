# 神经网络…在棍子上！

> 原文：<https://hackaday.com/2018/04/24/neural-networks-on-a-stick/>

他们的灵感可能不是来自棒上的[杰夫·敦哈姆的]墨西哥胡椒，但英特尔已经创造了 Movidius 神经计算棒，它实际上是 USB 棒形状因素中的神经网络。他们不依赖于云，他们不需要风扇，你可以用不到 100 美元买到一个。我们对[【杰夫·约翰逊】用 Pynq-Z1](http://www.fpgadeveloper.com/2018/04/setting-up-the-pynq-z1-for-the-intel-movidius-neural-compute-stick.html) 使用这些棍子很感兴趣。他还指出，这是在树莓皮或比格犬骨上放置神经网络能量的一个很好的方式。他向我们展示了 YOLO——一种图像识别器——并将其应用于 HDMI 信号，在 [Movidius](https://developer.movidius.com/start) 上完成处理。你可以在下面的第一个视频中看到结果。

起初，我们认为使用 Z1 的内置 FPGA 来做神经网络可能会更好。[Jeff]指出，虽然这是可能的，但 Z1 上有一个低端设备，因此没有太多 FPGA 空间可供使用。那么，棍子是个好主意。您可以在下面的第二个视频中了解更多关于该设备的信息。

在这些任务中有大量的处理工作在进行，只需拍摄一段视频就可以每秒 3 帧的速度进行处理，但使用软件缩放完整尺寸的速度下降到原来的一半。然而，[Jeff]认为如果他在 FPGA 中进行缩放，他可以轻松地将速率恢复到每秒 3 帧。

我们之前已经看过 Pynq 并且毫不怀疑它的名字和 PCB 颜色的来源。我们很想看到一些我们报道过的拥有视觉的[机器人被改装成使用这项技术。](https://hackaday.com/2016/10/09/tensorflow-robot-recognizes-objects/)

 [https://www.youtube.com/embed/D1RxIp76rpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D1RxIp76rpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/fESFVNcQVVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fESFVNcQVVA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

