# 降压转换器是如何工作的？

> 原文：<https://hackaday.com/2016/06/04/how-does-a-buck-converter-work-anyway/>

[Great Scott]应该获得对降压转换器的最快[解释奖。时长五分半钟的视频清晰地展示了该设备背后的工作原理。](https://www.youtube.com/watch?v=m8rK9gU30v4)

它从一个问题开始，如果你想降低一个电压，你应该怎么做？我们许多人都知道，我们可以使用 Arduino 上的 PWM 来调暗和点亮 LED，但用示波器仔细观察仍会发现 5V 峰值，这对 3.3V 电路来说是危险的。然后，他添加了一个电感和二极管，这可以防止电流下降过快，但 PWM 开关速度不够快，无法保持线圈通电。

对 Arduino 代码的一个小修改，PWM 频率现在在 kHz 范围内。示波器上的电压看起来很好，但滤波器电容使它看起来更好更平滑。最后，他展示了当负载改变时，输出电压看起来有什么不同。为了解决这个问题，分压器将信息反馈给 Arduino，让它改变 PWM 占空比以匹配负载。

在视频的最后一分钟，他展示了如何连接现成的开关调节器，随着基本原理的理解，其支持元件现在已经完全不再神秘。休息后的视频。

 [https://www.youtube.com/embed/m8rK9gU30v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m8rK9gU30v4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

