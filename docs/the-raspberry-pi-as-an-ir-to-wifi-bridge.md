# 树莓 Pi 作为 IR 到 WiFi 的桥梁

> 原文：<https://hackaday.com/2017/04/23/the-raspberry-pi-as-an-ir-to-wifi-bridge/>

[Jason]有一个 Sonos 家庭音响系统，有一堆通过 WiFi 连接的扬声器。[Jason]还有一个在没有 WiFi 的宇宙中设计制造的万能遥控器。声纳不能通过红外线控制。这里有一个明显的问题，但幸运的是，带 WiFi 的微型 Linux 电脑售价 10 美元，红外接收器售价 2 美元。[结果是一个 IR 到 WiFi 的桥梁](http://wsmlab.blogspot.com/2017/04/ir-volume-control-for-sonos-connect-amp.html)来控制所有这些“智能”家庭音频解决方案。

[Jason]唯一需要从通用遥控器控制他的 Sonos 的是一个红外接收器和一个 Raspberry Pi Zero W。电路很简单-只需将红外接收器的电源和接地连接到 Pi，并将接收器的第三个引脚插入 GPIO 引脚。新的，花哨的官方 Raspberry Pi Zero 外壳非常适合这个版本，允许一小块红外透明的环氧树脂从为 Pi 相机设计的孔中伸出。

软件方面，[杰森]求助于 Node JS， [LIRC](http://www.lirc.org/) ，一款解码红外信号的软件。定义了 GPIO 引脚后，[Jason]设置了驱动程序，并使用 Sonos HTTP API 向他的音频单元发送命令。这个版本的文本文件做了很多手脚，但是结果是不言而喻的:[Jason]现在可以用一个万能遥控器控制他家里的所有东西了。