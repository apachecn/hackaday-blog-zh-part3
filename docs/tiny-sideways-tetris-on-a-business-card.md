# 名片上小小的俄罗斯方块

> 原文：<https://hackaday.com/2018/05/20/tiny-sideways-tetris-on-a-business-card/>

每个人都认识俄罗斯方块，即使它是名片上横放的小小俄罗斯方块。[Michael Teeuw]设计了这些印刷电路板，它们带有小的有机发光二极管屏幕来显示联系信息。俄罗斯方块游戏实际上是一个隐藏的复活节彩蛋；长按其中一个按钮就会启动它。

[![](img/0610fef52e2faf49d52078552d8569d1.png)](https://hackaday.com/wp-content/uploads/2018/05/sideways-tetris-square-anim.gif) 事实证明，在 ATtiny85 微控制器上安装一个可玩的俄罗斯方块是一个挑战。使用像 [TinyOLED](https://github.com/richardkchapman/TinyOLED) 或 [Adafruit 的 SSD1306 库](https://github.com/adafruit/Adafruit_SSD1306)这样的资源来绘制线条和形状很容易，但是使用该方法在 128×32 有机发光二极管上绘制这些实时图形需要一个缓冲区大小，这不适合 ATtiny85 的可用 RAM。

为了解决这个问题，[Michael]通过动态计算要写入有机发光二极管的数据，避免了对屏幕缓冲区的需求。此外，最小的可能元素是一个 4×4 像素的正方形，这一事实减少了跟踪屏幕内容所需的总内存。因此，避免了通常需要的内存块用作屏幕缓冲区。[Michael]还详细介绍了 [PCB 设计](http://michaelteeuw.nl/post/163129358212/electrocard-part-1-the-design)和[电路板组装](http://michaelteeuw.nl/post/163688065337/electrocard-part-2-soldering)阶段，为那些对使用热空气回流和手工焊接相结合来组装卡的过程感兴趣的人提供帮助。

PCB 名片展示各种小聪明。[神奇的 8 球名片](https://hackaday.com/2018/04/05/magic-8-ball-business-card-will-answer-all-your-questions/)简洁得令人耳目一新，后来成为 [Arduboy](https://hackaday.com/2014/03/01/the-credit-card-sized-gameboy/) 的项目已经磨出切口，以更好地适应组件，保持一切都超级苗条。