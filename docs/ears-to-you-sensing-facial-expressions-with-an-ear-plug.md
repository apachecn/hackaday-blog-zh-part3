# 耳朵对你:用耳塞感知面部表情

> 原文：<https://hackaday.com/2018/05/24/ears-to-you-sensing-facial-expressions-with-an-ear-plug/>

电子产品越来越小，但人类的手指不会。这给高度嵌入式的可穿戴计算机带来了真正的挑战。当然，语音命令已经走过了漫长的道路，但它也有自己的挑战。在某些情况下，你可能不想口头命令你的博格植入物。也许你需要安静。或者你可能担心意外触发装置。德国的研究人员想用监控面部表情来代替。因此，为了抓拍一张照片，你可能会眨眼，并在你的眼睑内侧快进播放你的电影，也许你会向右看两次。你可以在下面看到关于这篇论文的视频演示。

这篇论文着眼于几种不同的解读面部动作的方法。有些相当烦人。然而，一项很有前途的技术使用了耳场感应(EarFS)。一个带有电极的耳塞可以感应到耳道中由面部肌肉运动引起的电变化。检查的其他技术包括肌电图，电容传感和不同形式的电场传感。

该团队确定了 25 种不同的面部表情，尽管他们为每种技术选择了最好的五种。当命令列表超过大约七个手势时，人们似乎开始忘记该做什么。

感知耳朵的电路是由 Eagle 发明的，并出现在论文中。一个仪表放大器和两个双通道运算放大器涉及一些非常高的电阻。该电路有多种选择，可以使用不同的滤波器实现单端或差分工作。有趣的是，为了测试，研究人员将一个小手指插入耳朵，感受耳道内各种面部表情的变化。

在静态设置和运动中使用设备进行测试。没有一项技术是完美的，但数据确实表明，如果你能以一种对消费者更友好的方式小型化和封装电路，它可能是有用的。

我们考虑过使用 OpenCV 来观察面部表情，但是虽然这对机器人来说是一件事，但是用你戴着的设备来做就很难了。我们想知道这种技术是否对指挥用处不大，而对[计算出你有多生气](https://hackaday.com/2012/04/04/facial-recognition-software-can-tell-when-youre-frustrated-with-xbox-live/)更有用。

 [https://www.youtube.com/embed/yrcbLIQoWRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yrcbLIQoWRk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

