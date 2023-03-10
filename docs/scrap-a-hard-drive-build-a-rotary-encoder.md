# 废弃硬盘，制造旋转编码器

> 原文：<https://hackaday.com/2018/01/07/scrap-a-hard-drive-build-a-rotary-encoder/>

对于控制的感觉有一些东西要说。无论是高品质开关令人满意的咔哒声，还是昂贵放大器上锅的黄油般触感，你与之互动的控件的触觉体验都很能说明一台设备。

【GreatScott！]知道这一点，他决定寻找一种替代品，而不是忍受廉价旋转编码器的颠簸和摩擦。他最终[探索了作为编码器的硬盘电机](https://www.youtube.com/watch?v=tjCJ3MlFt7g)，虽然结果并不完全是高分辨率的，但他可能有所发现。从拆除一些旧硬盘开始——省下那些磁铁吧！——[斯科特！]发现电动机属于四线或三线类型。他知道硬盘电机是无刷 DC 电机，他推断四引线电机的三个绕组采用星形配置，中性点连接到外部连接。一点示波器工作显示了当电机轮毂转动时预期的三相输出，随着旋转方向的切换，超前和滞后相位发生变化。电机与 Arduino 相连，构成了一个可行的编码器，后来通过将每一相发送到比较器并使用数字输入而不是使用 Nano 的 ADC 进行了改进。

看起来像[GreatScott！]的当前设置只对临时编码器的完整旋转做出响应，但我们打赌分辨率可以得到提高。也许[之前这篇关于将 BLDC 汽车公司转变为编码器的文章](https://hackaday.com/2017/01/18/use-a-brushless-motor-as-a-rotary-encoder/#more-239740)会有所帮助。

 [https://www.youtube.com/embed/tjCJ3MlFt7g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tjCJ3MlFt7g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

