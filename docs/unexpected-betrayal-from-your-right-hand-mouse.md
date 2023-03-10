# 你右手鼠标的意外背叛

> 原文：<https://hackaday.com/2016/08/09/unexpected-betrayal-from-your-right-hand-mouse/>

有些人真的很喜欢那种在 F-16 驾驶舱里不会完全不合适的电脑鼠标。这种鼠标可以启动一个浏览器，只需轻轻向左移动 38 个按钮中的一个，就可以打开车库门。然而，[这种力量能被用于邪恶的](https://www.insinuator.net/2016/07/your-mouse-got-sick-and-you-dont-know-it-aka-reverse-shell-via-mouse/)，而不仅仅是让他们电脑的客人感到沮丧吗？

我们听说过可信外设在之前[被重新用于邪恶的用途。有时它们甚至被](http://hackaday.com/2014/03/30/malware-in-a-mouse/)[改造](http://hackaday.com/2009/03/16/ultra-mouse-modification/)用于更加[良性的目的](http://hackaday.com/2010/09/30/usb-mouse-with-storage-added/)。这些都有一个共同的趋势。鼠标本身必须经过物理修改才能添加漏洞或功能。但是，具有宏支持的高级鼠标可以按原样用于漏洞。

这种情况下的例子是罗技 G 系列游戏鼠标。鼠标能够在其存储器中存储多个个人设置。这样，某人可以将鼠标带到多台计算机上，并且仍然可以使用它们的所有设置。[Stefan Keisse]发现每个按钮的宏的 100 个命令限制足以在目标计算机上获得完整的反向 shell。

考虑到意外按下这些鼠标上的辅助按钮是多么容易，攻击者需要做的就是在交付被破坏的鼠标后等待。休息后的视频。

 [https://www.youtube.com/embed/LiC1jnT6b68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LiC1jnT6b68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

