# 柴炉靠 Arduino 能源运行

> 原文：<https://hackaday.com/2016/03/06/wood-stove-runs-on-arduino-power/>

啊，可爱的怪物！通常是一个好的，简单的小黑客的死亡。但是一百次中有一次，一个小黑客并没有被额外的功能埋没，而是大步流星地吸收它们，开花结果成为一个美丽的系统。[rockfishon]的 Arduino 驱动的木材炉控制器是这些美丽的例外之一。(好吧，我们承认它可以使用更花哨的面板。)

他开始时非常简单，想要将热电偶连接到 Arduino，读取数值，并在温度过高时发出警报。但是谁能就此止步呢？仅仅一个空气挡板伺服远离闭环加热控制系统？所以[rockfishon]增加了一个显示器和几个按钮，并有一个系统可以让他的燃木炉在完全正确的温度下运行，即使是在没有人照看的晚上。额外的好处是，所有的事情都被记录下来供以后分析。

代码比较直接，[可以在这个 Gist](https://gist.github.com/rockfishon/9ff774cac8dc306963d6/2d7cdfda8622ca834ae21b5ce2a0e1bff0f32264) 里找到。如果你想自己制作，你需要一个 Arduino Mega，然后[可以在 OSHPark](https://oshpark.com/shared_projects/jCbp3Q2B) 拿到为你制作的控制板。从 Hackaday.io 项目页面上的评论来看，一些人已经尝试过了。在之前，我们已经[见过其他的柴炉监控黑客，但这是我们见过的第一个关闭控制回路的。非常酷。](http://hackaday.com/2016/02/08/a-wireless-wood-stove-monitor/)