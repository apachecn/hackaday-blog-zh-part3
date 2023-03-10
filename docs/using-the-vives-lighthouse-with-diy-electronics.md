# 用 DIY 电子产品使用 Vive 的灯塔

> 原文：<https://hackaday.com/2016/07/06/using-the-vives-lighthouse-with-diy-electronics/>

HTC Vive 是即将到来的虚拟现实战争的明显赢家，并准备进入 Apple Watch、智能家居设备、3Com Audrey 和微软 MSN TV 背后的神圣消费电子产品大厅。这意味着二手市场上很快会有很多 Vives，为一些非常酷的硬件的一些有趣的再利用打开了大门。

[Trammell Hudson]一直在摆弄 Vive 的灯塔，这是一个红外发射立方体，让 Vive 有方向感。这个简单的盒子没有什么特别的，它确实可以用来给任何微控制器项目提供一个方向传感器。

Vive 的 Lighthouse 是一项非常酷的技术，它使用了多个扫描红外激光二极管和一组 led，使 Vive 能够感知自己的方向。它通过从左到右和从上到下交替闪烁和扫描激光来做到这一点。可以从两个灯塔确定的相关测量值是从第一个灯塔开始的水平角度、从第一个灯塔开始的垂直角度和从第二个灯塔开始的水平角度。这就是你在 3D 空间定位 Vive 所需要的一切。

为了让一个简单的微控制器达到同样的效果，[Trammell]使用了一个 120°视野的快速光电晶体管。这种设置只能在距离灯塔大约一米的地方工作，但这对于测试来说已经足够了。

[Trammell]正在为 Arduino 和 ESP8266 开发一个灯塔库，到目前为止，一切正常。他只需要一点点代码就能把实验板的角度转换成灯塔的角度。这是一个很好的使能版本，它将允许很多人开发一些非常酷的东西，我们迫不及待地想看看接下来会发生什么。