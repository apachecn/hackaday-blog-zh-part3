# 遥控流式扬声器

> 原文：<https://hackaday.com/2017/09/14/remote-controlled-streaming-speakers/>

为了更好地利用备用的 Raspberry Pi Zero W 和一套 LogitechZ-680 环绕声扬声器，[Andre van Kammen]将它们组装在一起，使它们能够从他的手机播放流媒体音乐。

真正开始的是在 Pi 音乐盒发行上的磕磕绊绊，购买 pHAT [![](img/89924ae9f7b6ed3a040f9be3e70601b2.png) ](https://hackaday.com/wp-content/uploads/2017/09/3297911494265810821.jpg) DAC 奠定了基础。打开扬声器的控制器外壳，[Kammen]能够从一些终端获得 5V 的电源，即使扬声器处于待机状态——太棒了！—Pi 可以使用它。功率和音量通过 Pi 的 GPIO 引脚控制，使用二极管降低电压，防止短路。

现在，如何判断扬声器是开着还是关着？嗯，显示器连接器上的一个引脚在打开时会变为 4.3V，因此将一个 10k 电阻和一个二极管连接到该引脚是一个可破解的解决方案。完成有线连接后，事实证明可以将 pHAT DAC 塞进控制器外壳，GPIO 接头从后面伸出来，在没有其他外部导线的情况下安装 Pi——真是太棒了！

一个定制的 C++守护进程控制着卷，一个针对 Mopidy 的 Python 扩展保持卷同步。它被设置为在十秒钟的沉默后关闭，但要打开它，所有[卡门]需要做的就是在他的手机的 Mopidy 应用程序上点击播放，然后享受。

Raspberry Pi Zero [有助于许多](https://hackaday.com/2016/12/21/an-eye-catching-raspberry-pi-smart-speaker/)令人印象深刻的[音乐流媒体工具](https://hackaday.com/2015/12/10/audio-streaming-on-the-cheap-with-an-rpi-zero/)，但还有其他更非传统的方法在家里播放音乐。