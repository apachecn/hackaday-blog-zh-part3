# 把任何一只老鼠挂在橡子上

> 原文：<https://hackaday.com/2016/10/22/hook-any-mouse-to-an-acorn/>

Acorn 是伟大的 IT 巨头之一，它在个人计算机的崛起过程中崛起，然后变得默默无闻。然而，对于许多爱好者来说，这些电脑和 Commodore 64 一样重要，一样受欢迎。[Simon Inns] [做了一个很棒的适配器，将现代 USB 鼠标连接到这些旧盒子上。](http://www.waitingforfriday.com/index.php/USB_to_Quadrature_mouse_adapter)

经过三十年与人的互动，一个人可能很难找到一个适用于旧电脑的鼠标。最重要的是，即使你做了，这些老鼠可能是一个暗淡的经历开始。它们是在工业设计师被邀请玩电脑之前很久就被制造出来的，并且经常令人沮丧和怪异。至少可以说，棉签和酒精都参与其中。

[Simon]的盒子将一个普通的 USB HID 兼容鼠标转换成这些 8 位计算机喜欢的正交信号。然后，计算机会计算这些假脉冲，并愉快地移动光标。他对有用的转换盒并不陌生，他使用了一个 Atmel micro (AT90USB1287)和一套很好的 USB 外设。这些都被很好地打包到一个项目箱中。前面有一个开关可以选择模拟模式。

如果你自己想要一个，代码和原理图可以在他的网站上找到。正如你在下面的视频中看到的，该设备运行良好！

 [https://www.youtube.com/embed/Bml9uGo3Zws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Bml9uGo3Zws?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

