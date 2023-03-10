# 使用快速原型制作时钟

> 原文：<https://hackaday.com/2016/04/17/using-rapid-prototyping-to-make-a-clock/>

[Markus]就读于斯德哥尔摩皇家理工学院。在他的高级原型制作课上，他必须使用快速原型制作技术制作一些东西，例如 3D 打印机、激光切割机和试验板。他选择做一个看起来很棒的钟。

他开始用 CAD 设计整个东西。底座是在 Ultimaker 上 3D 打印的。世界时钟显示器是一块激光雕刻的丙烯酸树脂，他加热并弯曲以适应。他使用 Arduino 和 16×2 LCD 矩阵创建了一个简单的时钟程序，能够显示不同的时区。你选择他们的方式很聪明。

一条薄的黄铜带位于显示器的底部，它充当触敏电阻带。根据您按下它的位置，电阻会发生变化，Arduino 会切换到该时区。这是一个令人敬畏的传感器的巧妙使用，它真正给了这个项目一个很好的触摸。对于一个 6 周的学校项目来说还不错！

说到激光切割钟，看看这个由丙烯酸制成的[绝对荒谬的齿轮摆钟](https://hackaday.com/2015/03/24/laser-cut-clock-kicks-your-cad-tools-to-the-curb-and-opts-for-python/)！

[通过 [r/DIY](https://www.reddit.com/r/DIY/comments/4e56zp/i_made_a_world_clock/)