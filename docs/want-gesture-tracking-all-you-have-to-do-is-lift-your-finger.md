# 想要手势追踪吗？你所要做的就是举起你的手指。

> 原文：<https://hackaday.com/2017/05/02/want-gesture-tracking-all-you-have-to-do-is-lift-your-finger/>

看着托尼·斯塔克挥动双手操纵投影结构是一个日益逼近的现实——至少在手势追踪方面是如此。lift——由加州大学欧文分校和 FX 帕洛阿尔托实验室的一个团队制造的原型——能够以 1.7 毫米的精度跟踪多达十个手指！

Lift 的手势跟踪是通过使用一个 DLP 投影仪、两个 Arduino MKR1000s 和一个针对每个手指的光传感器来实现的。Lift 的设计允许它在几乎任何平坦的表面上工作；投影图像充当用户的网格和工作区域。当他们的手指在投影表面上移动时，光传感器将图像信息输入 Arduinos，Arduinos 推断出每个手指的位置，并将其转化为数字工作空间。传感器也可以安装在其他物体上以增加功能。

到目前为止，该团队已经使用 Lift 作为绘图的输入设备，并使用它在标准的笔记本电脑屏幕上假装手势控制。下一步将是两个或更多的投影仪，这将允许 Lift 在三维空间中完全有效地工作，并直接与投影的媒体内容进行交互。它也能无线操作吗？是的。是的，可以。

虽然我们还没有托尼·斯塔克的全息工作站，但我们仍然可以[玩俄罗斯方块](http://hackaday.com/2016/05/28/hand-gestures-play-tetris/)、[驾驶无人机、](http://hackaday.com/2014/10/16/controlling-a-quadcopter-with-gestures/)和摆弄[手术机器人](http://hackaday.com/2016/06/16/arduino-meets-da-vinci-in-a-gesture-controlled-surgical-robot/)。