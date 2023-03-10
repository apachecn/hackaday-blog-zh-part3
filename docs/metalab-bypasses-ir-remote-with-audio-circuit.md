# Metalab 通过音频电路绕过红外遥控器

> 原文：<https://hackaday.com/2015/11/27/metalab-bypasses-ir-remote-with-audio-circuit/>

红外遥控器很棒，除非你在一个充满疯狂闪烁的灯光和各种随机红外辐射的黑客空间。那么，他们就是不可靠。奥地利维也纳金属实验室的一些聪明人用几个晶体管和一些音频软件去掉了红外中间人。他们称这个项目为 HDMI 耳语者，这是一个很可爱的设计。

Metalab 的 AV 系统有一个[网络前端](https://metalab.at/wiki/Slackomatic)，所以没有人*曾经*必须站起来，除非他们想站起来。他们买了一个非常便宜的 [5 比 1 HDMI 开关](http://www.aliexpress.com/item/Mini-5-Port-1080P-HDMI-Splitter-Switch-Switcher-Box-Selector-With-IR-Remote-Splitter-5port-HDMI/1578147382.html)来切换显示多个视频流。但是如何将交换机连接到 Raspberry Pi 服务器呢？

幸运的是，这个特殊的开关有一个远程安装的红外接收器，通过立体声音频插孔连接到主机。将这种传感器插入笔记本电脑，在按下遥控器按钮的同时运行 [Audacity](http://web.audacityteam.org/) 就可以获得播放遥控器代码的音频文件。只需通过一个微小的晶体管电路将这些从树莓 Pi 的音频输出播放到开关的红外输入即可。现在他们有一个联网的五路 HDMI 开关，价格为 10 美元。

鉴于大多数红外遥控器的低数据速率，我们可以想象对具有内置红外接收器的设备使用相同的技巧。只需夹出红外接收器和焊接在一对夫妇的电线，然后直接注入你的“音频”信号。

但是 IR hacks 很有趣。我们在这里已经看到了很多，从经典的[相机快门释放黑客](http://hackaday.com/2011/12/08/ir-remote-for-dslr-cameras/)到更一般的关于用 Arduinos 克隆红外信号的[教程。](http://hackaday.com/2013/11/20/primer-tutorials-for-arduino-ir-remote-cloning-and-keyboard-simulation/)

感谢[overflo]的提示！