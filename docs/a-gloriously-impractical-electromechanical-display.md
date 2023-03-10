# 极其不实用的机电显示器

> 原文：<https://hackaday.com/2017/12/19/a-gloriously-impractical-electromechanical-display/>

对于今年的办公室假日派对，[Gavan Fantom]想做一些真正特别的事情。同事们正在摆弄发光二极管来设计显示器和装饰品，但他们缺乏机械显示器的老派感觉。他想创造一些具有运动元素复古外观的东西，但不想只是重现我们一再看到的传统翻转机制。

[![](img/4019be99af45d6b45f51260b0460e4fd.png)](https://hackaday.com/wp-content/uploads/2017/12/elecdisp_detail.jpg)

The mechanism to drive a single “pixel”.

[【Gavan】想出的是惊人的不切实际的 8×8 显示器，听起来和看起来一样酷](http://www.coolfactor.org/project/pixel/)。显示器中的每个“像素”都是一个由业余爱好伺服系统旋转的 3D 打印螺旋机构。当像素在其外壳中旋转时，它对于观察者来说变得越来越明显。甚至可以通过改变旋转角度来调整像素的不透明度，从而允许灰度图像的基本显示。

显示器中的每个元素都由七个 3D 打印部件和两个钉子组成，机械装置在其上滑动以向前和向后移动。一个 8×8 的显示器需要 64 个元件，这意味着整个显示器需要 64 个伺服系统、128 个钉子和 448 个庞大的 3D 打印部件。即使两台打印机并行工作，仅打印一项就花了两周多的时间才完成。

该显示器由一个树莓 Pi 和三个“ [Mini Maestro](https://www.pololu.com/product/1356) ”控制器驱动，每个控制器可以处理 24 个伺服系统。[Gavan]在 Python 中找到了一些样本代码来将命令传递给 Maestro 伺服控制器，他在编写自己的软件时使用这些代码作为模板。Python 脚本打开图像文件，将其转换为灰度，然后将每个像素的值映射到相应伺服的旋转。他说这个软件有点粗糙，还有一些校准工作要做，但是我们认为到目前为止结果是惊人的。

[机械显示器是黑客们的最爱](https://hackaday.com/2013/11/04/hacking-a-flip-dot-display/)，在[很大程度上是因为它们在运行时发出的可怕噪音](https://hackaday.com/2015/01/14/the-giant-flip-dot-display-at-ces/)。[虽然在](https://hackaday.com/2015/04/25/lego-flip-dot-display/)之前我们已经看到了一些非常有创意的展示方式，但【加万】在这里创造的东西肯定是独一无二的。

 [https://www.youtube.com/embed/0MbeUOh8Fto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0MbeUOh8Fto?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/jw7q_kcQXO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jw7q_kcQXO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

