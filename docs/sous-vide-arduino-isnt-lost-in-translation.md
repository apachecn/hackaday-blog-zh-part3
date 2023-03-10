# Sous Vide Arduino 没有在翻译中丢失

> 原文：<https://hackaday.com/2017/04/27/sous-vide-arduino-isnt-lost-in-translation/>

如果你认为六道菜的一餐是一小份鸡块，那你可能错过了炖肉在厨师中的兴起。这个想法是你把食物密封在一个塑料袋里，然后在一个温度精确的水浴中烹饪。这个温度比你通常使用的温度低得多，所以烹饪时间很长，但结果是食物被均匀地烹饪，并且在烹饪过程中不会失去太多水分。当然，控制温度对于微控制器来说是一项完美的工作，而且[Kasperkors]已经使用 Arduino 进行了自己的设置。帖子是丹麦语，但是[谷歌翻译](https://translate.google.com/translate?hl=en&sl=da&tl=en&u=http%3A%2F%2Fwww.instructables.com%2Fid%2FSous-Vide-Ala-Arduino%2F)好得惊人。

这个吸引人的设置使用了一个 Arduino Mega、一个显示器、一个防水温度探头和一些零碎的东西。翻译在零件清单上确实有点失败，但是如果你用“ground”代替“earth”和“soil ”,你应该是安全的。对于真正的伊壁鸠鲁主义者来说，形式和功能一样重要，内置 led 的丙烯酸盒子当然引人注目。你可以在下面看到这个设备的视频。

开关、发光二极管和继电器都是标准配置。该项目的真正核心是温度控制。许多控制器使用 [PID](https://hackaday.com/2016/05/18/flying-with-proportional-integral-derivative-control/) (比例/积分/微分)来保持温度，但这个项目采取了一种更务实的方法。根据温度与设定点的距离，控制器简单地以不同方式驱动加热元件，并或多或少地频繁测量以进行调节。例如，如果温度低两度以上，加热元件会持续开启。当它靠近时，加热元件运行 10 秒，等待 5 秒，然后算法再次读取温度。

关于温度应该有多精确有很多争论。显然，对于像鱼这样的东西来说，大范围的温度不是问题。然而，鸡蛋需要更严格的控制，因为它们的蛋白质会变性(不管这意味着什么)。

还有一个安全继电器，如果温度变得很高或很低，它会关闭整个事件，这样一个坏的温度传感器就不会把一切都烧干。我们可能会考虑用双金属线圈来做这件事，这样即使 Arduino 出现故障也不会阻止它工作。

我们已经看到了其他[吸引人的视频设置](https://hackaday.com/2011/11/13/sous-vide-with-racing-stripes/)。更不用说用[一个瓦罐](https://hackaday.com/2011/08/09/sous-vide-crock-pot-controller/)制作的更加实用的建筑了。不管它看起来像什么，这些项目可能不会帮助你的腰围。

 [https://www.youtube.com/embed/6TrtcnOcWfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6TrtcnOcWfI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

