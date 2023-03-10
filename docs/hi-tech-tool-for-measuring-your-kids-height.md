# 测量孩子身高的高科技工具

> 原文：<https://hackaday.com/2016/09/22/hi-tech-tool-for-measuring-your-kids-height/>

当然，我们可以让我们的孩子背靠着墙，强迫他们站直，并在他们的头上用尺子在墙上标出他们的身高，但我们会是什么样的黑客呢？不涉及任何微控制器或任何电子元件！自称为[自制垃圾]的 DIY 家庭挺身而出，发明了一种高科技工具来测量他们孩子的身高。

他们用一个小木箱代替尺子放在头上。在盒子下面，在面向下的后端，他们安装了一个 [VL53L0X 激光测距传感器](http://www.st.com/content/st_com/en/products/imaging-and-photonics-solutions/proximity-sensors/vl53l0x.html)。它有 2 米的范围，任何孩子都可以使用。但是盒子必须平放在孩子的头上，否则激光会以一个角度指向下方。为了解决这一问题，他们在盒子里放了一个 MPU6050 6 轴运动传感器，以及一个 Arduino Nano，将它们连接在一起。LCD 显示器、测量按钮和 LED 安装在盒子外面的后向侧。

要使用它，父母将盒子放在孩子的头上，确保激光传感器没有被阻挡，并且可以看到地板。LCD 显示高度，以及 x 和 y 方向的加速度。如果箱子不水平，LED 为红色；如果水平，LED 为绿色。按住测量按钮将工具置于测量模式，当它水平时，LED 变为蓝色，LCD 显示屏冻结，因此您可以记下高度。你暂时是好的，取决于你孩子的年龄。看到它被用来衡量一个孩子休息后，以及一个额外的剪辑显示什么样的输出时，挥舞着一只手上下下方。

在这里，他们测量孩子的身高。

 [https://vine.co/v/51TtuvLnUId/embed/simple](https://vine.co/v/51TtuvLnUId/embed/simple)



这是在传感器下面举起和放下手时的输出。x 和 y 值是来自运动传感器的加速度值。

 [https://vine.co/v/51TIIe0311j/embed/simple](https://vine.co/v/51TIIe0311j/embed/simple)



说到测量我们孩子的参数，看看这个[机器人医生，它读取孩子的脉搏而不会吓到他们](http://hackaday.com/2012/08/28/robo-doc-reads-childrens-pulses-without-scaring-them/)。

[via [hackster.io](https://www.hackster.io)