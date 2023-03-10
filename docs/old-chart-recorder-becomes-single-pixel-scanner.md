# 旧图表记录器变成单像素扫描仪

> 原文：<https://hackaday.com/2017/07/08/old-chart-recorder-becomes-single-pixel-scanner/>

有这么多从纸上捕捉图像的方法，我们真的需要另一种吗？尤其是一个需要 15 分钟拍摄 128×128 像素图像的？可能不会，但是构建一个单像素 RGB 扫描仪很有启发性，而且非常有趣。

我们不得不承认，不久前当[Kerry Wong]得到一个古老的惠普 X-Y 图表记录器时，我们想知道它是否会带来任何有用的东西。有人可能会吹毛求疵，声称他用它建造的洛伦兹吸引子绘图仪是有用的，这个单像素扫描仪同样值得怀疑，但我们喜欢这个想法。使用 Arduino 驱动记录器的 X 轴和 X 轴通过床上的光栅图案，并用 RGB 传感器板代替笔，[Kerry]能够收集每个像素的颜色数据并重建图像。如果你没有模拟 X-Y 记录器，复制这一点不会太难，这只是表明，不是所有东西都需要步进机和数字才能完成有用的工作。或者至少是半有用的。

至于使用的 RGB 传感器，他们之前已经在这里出现过很多次，主要是在 [M & M 分类器](https://hackaday.com/2016/12/16/anti-entropy-machine-satiates-mm-ocd/)中，但偶尔会有[联觉模拟器](https://hackaday.com/2015/11/18/smell-colors-with-a-syntesthesia-mask/)。

 [https://www.youtube.com/embed/U5PwsVqHT8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U5PwsVqHT8Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

