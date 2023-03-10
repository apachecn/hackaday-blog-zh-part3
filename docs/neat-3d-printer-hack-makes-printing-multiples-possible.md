# 简洁的 3D 打印机技术让打印多份成为可能

> 原文：<https://hackaday.com/2018/07/04/neat-3d-printer-hack-makes-printing-multiples-possible/>

3D 打印的承诺之一是你可以在家里大规模生产物品，打印出你想要的任何东西的多个副本。不幸的是，现实有点不同:一旦你打印出了一些东西，你通常需要手动将其从打印床上移除。除非你是[Replayreb]，那就是:他想出了一个巧妙的方法，通过使用 g 代码的[自定义位来移动打印头，将打印下来的内容放到等待框](https://www.thingiverse.com/thing:2976776)中，从而将打印内容从打印床上移除。

 [https://www.youtube.com/embed/I69kK5qjOQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I69kK5qjOQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Replayreb]想出这个主意是因为他在 Etsy 上销售 [Lightsabre 笔帽，并希望尽可能实现打印自动化。所以，他写了一小段 g 代码来保持打印床的温度，移动打印头靠近打印床并向上移动。把指纹从床上弄掉。他还想出了一个简短的 Windows 脚本，加载打印 g 代码，添加额外的代码来删除它，并创建两者的多个副本。设定此打印，打印机将自动生成对象的多份副本。](https://www.thingiverse.com/thing:2976776)

不过，这种方法有其局限性:它只能用于像[Replayreb]的 Lightsabre 这样的高而薄的印刷品，这些印刷品的表面积很小，在推动时会干净地离开印刷层。还必须将打印机设置为在打印床边缘附近打印。因此，对于每一种不同的印刷品，都需要一些调整和练习。

回到过去的美好时光，Makerbot 确实生产了一个[带打印表面](https://www.thingiverse.com/thing:4056)来做类似的事情，我们在过去已经看到了[许多类似的想法](https://hackaday.com/2018/04/29/towards-more-automated-printers/)，但这两者都需要额外的硬件。这种方法使用打印机本身，不需要任何东西，只需要一点 g 代码的小聪明。