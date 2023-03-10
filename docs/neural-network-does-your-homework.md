# 神经网络做你的功课

> 原文：<https://hackaday.com/2017/02/17/neural-network-does-your-homework/>

[Will Forfang]发现了一个应用程序，它可以让你用手机拍下一个数学方程，并寻求解决方案。然而，该应用程序无法读取手写方程，所以[威尔]决定使用神经网络来看看这有多难。

[结果](http://www.willforfang.com/computer-vision/2016/4/9/artificial-intelligence-for-handwritten-mathematical-expression-evaluation)相当令人印象深刻(你也可以看下面的视频)。[威尔]用他自己的笔迹写在黑板上，让网络在上面训练。他还更进一步，添加了一些启发式方法来识别分数条，并根据条的相对大小来推断分组。

神经网络代码很简单，但是有很多节点。捕获的图像为 75×75 或总共 5，626 像素。每个像素都有一个神经元。这些神经输送到 50 个中间神经元。软件可以识别的 18 个符号(数字、数学运算符等)中的每一个都有一个神经元。

编程只是为了得到神经元算法。实际的字符识别是通过使用示例输入数据训练网络来处理的——在黑板上一遍又一遍地写数字。一旦方程被识别，就不难求解实际方程(据我们所知，这不是通过神经网络完成的)。

我们已经看到神经网络在做[语音生成](https://hackaday.com/2016/12/03/talking-neural-nets/)、[飞行直升机](https://hackaday.com/2014/04/22/self-learning-helicopter-uses-neural-network/)，甚至[喷不需要的猫](https://hackaday.com/2016/07/08/neural-network-targets-cats-with-a-sprinkler-system/)。

 [https://www.youtube.com/embed/nF0I4gILeOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nF0I4gILeOs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示[约翰]。