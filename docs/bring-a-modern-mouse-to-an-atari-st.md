# 把一只现代老鼠带到雅达利街

> 原文：<https://hackaday.com/2017/01/23/bring-a-modern-mouse-to-an-atari-st/>

人类输入设备是今天我们计算机上的消耗品。它们是如此的便宜和标准化，以至于当一个鼠标或键盘过期时，我们不会想第二次，只是扔掉它，再买一个。不管我们有什么样的电脑，它都能正常工作，我们可以不停地工作。

但是在早期的机器上，我们可能没有这么幸运。第一代带鼠标的电脑没有 USB，甚至没有 PS/2 或串行接口，而是有各种各样的专有鼠标接口，通常携带直接来自外围设备旋转传感器的正交信号。如果你有一个正交鼠标死了，那么你就有麻烦了，因为你不容易找到一个新的。

幸运的是，有一个解决方案。在这之间的几十年里，计算能力的价格已经下降到这样的程度，你可以购买一台单板计算机，它的能力远远超过与标准 USB 鼠标的接口，并同时模拟正交鼠标。这正是[Andrew Armstrong]为他的 Atari ST 提供替代鼠标所采用的解决方案，他[通过 GPIOs 将 Raspberry Pi 用作 USB 主机和正交鼠标仿真器](https://www.youtube.com/watch?v=ED3PSM4Mwss)(YouTube 链接)。

他在我们放在休息时间下方的视频中对他的工作进行了全面的描述，同时，如果你想亲自体验一下[，你可以在他的 GitHub 知识库](https://github.com/backofficeshow/ATARIPiMouse)中找到你需要知道的一切。

 [https://www.youtube.com/embed/ED3PSM4Mwss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ED3PSM4Mwss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



这不是我们在这里看到的第一个 USB 到正交仿真器，去年我们展示了另一个项目[使用 Atmel 微控制器为 Acorn Archimedes](http://hackaday.com/2016/10/22/hook-any-mouse-to-an-acorn/) 做同样的事情。