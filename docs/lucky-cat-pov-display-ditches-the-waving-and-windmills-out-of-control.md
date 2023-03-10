# 招财猫视点显示沟渠挥舞和失去控制的风车

> 原文：<https://hackaday.com/2018/05/15/lucky-cat-pov-display-ditches-the-waving-and-windmills-out-of-control/>

如果你去过日本餐馆，你可能会看到招财猫，一只猫向你招手表示欢迎。它被认为会带来好运，但我们不确定[马丁·菲茨帕特里克]是否在用这只招财猫 POV 显示器来推波助澜。他黑掉了其中一个小雕像，这样手臂就形成了一个视觉暂留(POV)显示器，爪子上闪烁的 led 灯创造了一个点阵式的显示器。

在这只倒霉的猫体内，有一个韦莫斯·D1 电机驱动器和一些其他部件，可以把这只猫变成一台工作显示器。他安装在爪子上的五个发光二极管足够宽，可以显示 5×7 个字符。机械设计中棘手的部分是将信号从一个固定的基座传递到一个旋转的臂(自然界)。在这种情况下，使用 Adafruit 的[6 线滑环可以轻松解决问题。[马丁]使用一个刷 DC 电机和几个齿轮加速招财猫。](https://www.adafruit.com/product/736)

ESP8266 正在运行 MicroPython——这种组合应该可以轻松地连接到您想要显示自己的消息的任何 web 服务 API。现在，手臂没有位置意识，所以信息不会像使用霍尔效应传感器那样锁定在一个位置。但是[马丁]说，这只猫的内部还有足够的空间，未来的升级可能包括将电池藏在里面，形成一个无线的一体化建筑。如果他接受了这一点，那么这也是添加某种轴编码的绝佳时机。

检查休息后在剪辑中炫耀的招财猫。

> [Python 驱动的 Maneki-neko 视觉暂留滚动器](https://imgur.com/TBcplph)