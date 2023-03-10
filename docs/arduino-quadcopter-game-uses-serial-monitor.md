# Arduino 四轴飞行器游戏使用串行监视器

> 原文：<https://hackaday.com/2016/04/23/arduino-quadcopter-game-uses-serial-monitor/>

每一代新计算机都重复前几代使用的技术。[Kim Salmi] [使用 Arduino 串行监视器上显示的 Arduino 创建了一个基于 ASCII 的四轴飞行器模拟游戏](http://tunn.us/arduino/quadcopter.php)。现代的变化是控制器:一个加速度计补充了操纵杆，以实现身临其境的游戏。当然还有闪烁的 led。

Arduino Uno 提供处理能力并驱动串行监视器。操纵杆和日立 H48C 加速度计安装在试验板上，并连接到 Uno。加速度计的倾斜控制着屏幕上四轴飞行器的高度和左右运动。操纵杆将直升机设置在悬停模式，并放下一条救援绳。当达到最大高度(屏幕的垂直极限)时，另一个 LED 会发出警告。操纵杆还选择三个四轴飞行器中的一个，它们具有不同的性能特征。

休息之后有一段视频。[Kim]提供了源代码，因此您可以将其用作处理操纵杆和加速度计输入的参考。

更多的证据表明旧的就是新的。

 [https://www.youtube.com/embed/bsvGAcvknPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bsvGAcvknPw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

