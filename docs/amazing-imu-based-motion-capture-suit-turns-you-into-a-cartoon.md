# 令人惊叹的 IMU 动作捕捉套装将你变成卡通

> 原文：<https://hackaday.com/2016/01/23/amazing-imu-based-motion-capture-suit-turns-you-into-a-cartoon/>

阿尔瓦罗·费伦·希福恩特斯制作了我们在好莱坞之外见过的最酷的动作捕捉套装。它基于将一堆惯性测量单元(IMU)绑在他的身上，将数据发送到计算机，并进行一些合理的严肃数学运算。这简直太棒了，而且完全可以用 DIY 预算完成。看看下面的视频，你会大吃一惊的。

手机都使用 IMU 来提供诸如点击检测和屏幕旋转信息等有用的功能。这意味着它们变得便宜了。在一个小芯片上测量九个自由度的能力，对于 chicken scratch 来说，几乎使这种发展成为必然，正如我们在 2013 年看到一个单臂概念验证后提出的那样。

但是[阿尔瓦罗]已经超越了。一切都是开源的，并记录在他的 GitHun 上。一个 Arduino 读取绑在他四肢上的传感器板(通过多路 I2C 线)，并通过蓝牙将数据发送到他的电脑。在那里，一个 Python 脚本接管并将数据传递给 [Blender](https://www.blender.org/) ，后者实时渲染一个 3D 模型进行匹配。

所有这些意味着你现在就可以在家里以低廉的价格复制这个不可思议的项目。我们不知道这将走向何方，但它会很酷。

 [https://www.youtube.com/embed/JddtxynTgLk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JddtxynTgLk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

