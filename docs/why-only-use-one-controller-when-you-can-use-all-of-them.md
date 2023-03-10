# 当您可以使用所有控制器时，为什么只使用一个控制器？

> 原文：<https://hackaday.com/2017/10/28/why-only-use-one-controller-when-you-can-use-all-of-them/>

在启动他的 RetroPie 系统后，[jfr miller]明显感觉有什么不对劲。意识到现代的 Xbox 360 控制器不适合重温他年轻时的游戏，他收集了他所有的 [![](img/b6f12b5b1bb08a8f00f7ab612b96ff80.png)](https://hackaday.com/wp-content/uploads/2017/10/multijoy19.jpg) 旧控制器，以确保他总是有适合游戏的[游戏手柄。](https://jfrmilner.wordpress.com/2017/10/16/retro-gaming-system/)

想要保持控制器不被修改——因此它们仍然可以在原始系统上使用——他必须做一些逆向工程，并在构建控制器中枢之前采购一些控制器插座。利用移入寄存器、移出寄存器和一些多路复用器，他设计了一个大电路选择器——它充当 Arduino 微处理器的屏蔽——因此所有控制器都保持连接。一个电位计允许他选择想要的控制器和几个拱廊按钮，这些按钮访问 RetroPie 快捷方式真正完善了中枢。休息之后来看看演示吧！

 [https://www.youtube.com/embed/LYXYafwz_CY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LYXYafwz_CY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[jfr miller]保留了与他将要玩的游戏相关的控制器，但我们希望在他的构建中有一些空间来包含一个 rug 格式的控制器。当然，总有选择[偷工减料旧系统](https://hackaday.com/2017/10/06/an-old-video-game-controller-on-even-older-computer/)使用你喜欢的复古游戏手柄。