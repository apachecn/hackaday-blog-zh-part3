# 太阳能控制器双向逆向工程

> 原文：<https://hackaday.com/2017/01/27/solar-controller-reverse-engineered-in-both-directions/>

[Jared Sanson]在他的海滨别墅里有一个太阳能装置，由 6 块电池板和一个 24V 电池组组成，由 Outback Inc .提供。它们的充电器和逆变器通过一个看似专有的连接与一个名为 MATE 的控制器配对。MATE 有一个标准的串行输出，提供了一些关于操作的细节，但[Jared]没有从控制器的屏幕上获得详细的信息。这意味着是时候对专有连接进行逆向工程了，Jared 称之为 MateNET。

控制器通过 Cat5 电缆与充电器连接。[Jared]最初怀疑是 RS-485，但结果是 0-24V 逻辑电平的常规串行，9600 波特，9n1。为了找出引脚排列，[Jared]用细齿梳仔细检查了 MATE 电路，发现了一个 ATMEGA32。由于 MATE 的用户输出及其与其他设备的连接都是串行的，所以使用一个逻辑多路复用器在两个串行连接之间分割 ATMEGA32 的单个 UART。随着物理层的分类，是时候弄清楚协议是如何工作的了。

第一步是从运行的系统中捕获一些数据包，将 MATE 连接到 MX 充电控制器。MateNET 系统使用第 9 位来表示数据包的开始，这有些困难——[ Jared]的 PC 嗅探设置忽略了这个奇偶校验位。通过将捕获的数据包内容与屏幕上显示的内容进行匹配，可以确定包含状态、电池电压和太阳能电池板电压的字段。然而，包的其余部分不容易理解，因此[Jared]决定改变策略。

使用 Python 模拟 MX 充电控制器，将包含不同内容的数据包发送给伴侣，并监控屏幕变化。这种欺骗方法使得数据包的内容更容易确定。重要的是要注意数据包中使用的校验和，以确保配偶认为数据有效。[Jared]走得更远，试图用他的 Python 代码欺骗其他硬件。MATE 帮了大忙，当来自不同硬件的数据包比预期的要短或格式不正确时，它会显示出来，帮助他们猜测正确的格式。这些工作都被打包到 [pymate](http://jared.geek.nz/pymate) 中，这是一个 mate 控制器的 Python 仿真器。

随着协议的制定，是时候结束这个项目了。在 Carambola2 Linux 板上运行 pymate，处理数据包并最终存储在远程服务器上的 PostgresSQL 数据库中。将这与令人惊叹的 Grafana 开源图形库结合起来，允许[Jared]通过一些非常漂亮的图形帮助查看他的系统状态，通过一个允许库搜索 SQL 的[Github 分支。](https://github.com/sraoss/grafana-sqldb-datasource/releases)

这是一个整洁的项目，具有非常专业的最终产品，并允许[Jared]轻松地远程监控他的太阳能设置。电力监控黑客非常受欢迎——我们甚至看到用 Python 用[网络摄像头监控电表。](https://hackaday.com/2014/12/29/reading-power-use-data-with-a-webcam-and-python/)