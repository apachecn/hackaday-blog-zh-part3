# 完全简单的超声波数据通信

> 原文：<https://hackaday.com/2018/06/01/dead-simple-ultrasonic-data-communication/>

一些最好的黑客是那些事后看来非常明显的；一个如此优雅的解决问题的方法，你会奇怪你以前怎么从来没有想到过。当然，我们也喜欢那些复杂到让你开始流眼泪的黑客，但是有一个平衡是很好的。这一个，由爱德华多·佐拉送来的，绝对属于前一组。

[![](img/16c7a39d8c480fbbbd0bc267c6040d7a.png)](https://hackaday.com/wp-content/uploads/2018/05/ultrasonic_detail.jpg) 在休息后的视频中，【Eduardo】演示了他为[使用超声波传感器进行单向数据通信](http://www.zolalab.com.br/eletronica_projetos/ultrasonic_talk.php)的极其简单的设置。由一对 Arduinos 驱动，使用从非常受欢迎的 HC-SR04 模块中回收的传感器，很多读者很有可能在自己的工作台上用身边的东西重现这一台。在这个例子中，他将文本字符串从一台计算机发送到另一台计算机，但只要稍加想象，这可以用于各种项目。

对于发射器，超声波传感器只需连接到 Arduino 上的一个数字引脚。接收器稍微复杂一点，需要一个 LM386 放大器和 LM393 比较器来产生一个干净的信号，供第二个 Arduino 读取。

但是它是如何工作的呢？通过查看发送器和接收器的源代码，我们可以看到这是最基本的。发送器 Arduino 将给定的字符串分解成单个字符，然后进一步将 ASCII 转换成八个二进制位。这些比特以音调的形式发送出去，并在接收端被接收。一旦接收器收集到相当多的音调，它就会处理这些音调，并将二进制值转换回 ASCII 字符，然后通过串行方式发送出去。很*慢*，但是很简单。

如果你正在寻找更强大的东西，看看这个关于使用 GNU 无线电和超声波的 T2 指南。

 [https://www.youtube.com/embed/25FJy9Wcn9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/25FJy9Wcn9I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

