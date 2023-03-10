# 用显卡解迷宫

> 原文：<https://hackaday.com/2017/10/23/solving-mazes-with-graphics-cards/>

如果我们告诉您，您的计算机数量可能比您想象的要多，会怎么样？我们不是在谈论那些看起来不像电脑的东西，比如大多数现代汽车或某些灯泡。我们谈论的是藏在你的台式电脑里的强大机器，叫做“显卡”。在普通游戏装备中，比内置显卡更强大的显卡很常见。在他的教程中[Viktor chlumsk]展示了如何利用你的 GPU 的能力来解决一个迷宫。

运行在 GPU 上的软件被称为[着色器](https://en.wikipedia.org/wiki/Shader)。在这个示例中，显示了一个着色器，它找到了通过迷宫的方法。我们还可以一瞥使这个软件领域变得特殊的局限性:[Viktor]的解决方案只能处理四个变量，因为所有信息都存储在图像的红色、绿色、蓝色和 alpha 通道中。阿尔法通道代表迷宫的边界。红色和绿色通道用于从迷宫的起点和终点广播电波。这两个波相遇的地方是最短的解，一个通过蓝色通道捕获的值。

尽管拥有大量内核和大容量内存，但对着色器编程感觉更像是在微控制器上工作。自己看看下面的迷宫解决步行通过。

 [https://www.youtube.com/embed/GULy4vtkw6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GULy4vtkw6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



如果我们已经让你迷上了 GPU 编程，请睁大眼睛，还有更多在路上。在那之前，你可能喜欢从[命令行](https://hackaday.com/2012/05/30/gpu-programming-for-easy-fast-image-processing/)创建像素着色器，或者用它们来驱动带 VGA 的[ws 2811 led](https://hackaday.com/2016/01/04/driving-ws2811-leds-with-vga/)。