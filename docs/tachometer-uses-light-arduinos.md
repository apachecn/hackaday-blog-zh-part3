# 转速表使用灯，Arduinos

> 原文：<https://hackaday.com/2018/02/24/tachometer-uses-light-arduinos/>

为了测量一件东西旋转的速度，我们大多数人会去拿转速表，而不去想它是如何工作的。转速表通常在汽车上用来测量发动机的转速，但是手持设备也可以用来测量其他东西的转速。虽然有些机械轴必须与你试图测量的任何东西进行物理接触，但[electronoobs]创造了一种[非接触式转速表，它使用红外光来测量转速](http://www.electronoobs.com/eng_arduino_tut15.php)。

该工具使用红外发射器/检测器对和运算放大器来检测转速。来自红外探测器的信号通过运算放大器，以改善信号质量，然后馈入 Arduino。该设备还具有有机发光二极管屏幕和微调电位计，所有这些都位于其独立的 3D 打印外壳中，由 9 V 电池供电，最高可测量 10，000 RPM。

这种设计的唯一缺点是需要在对象身上贴一片白色胶带，以使红外探测器正常工作，但这是一种可以接受的折衷，因为不必与高速旋转轴进行物理接触。如果你想构建自己的工具，所有的原理图和 g 代码都可以在项目网站上找到，如果你想知道 Arduino 还使用了哪些工具，请务必查看基于 Arduino 的精密夹具。

 [https://www.youtube.com/embed/uiWo-GEW4xg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uiWo-GEW4xg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

