# 从 Pi 传输 Tee Vee

> 原文：<https://hackaday.com/2015/11/27/transmitting-tee-vee-from-a-pi/>

想建立自己的电视台吗？这个黑客可能会有所帮助:[Jan Panteltje]已经研究出如何将一个[树莓 Pi 变成一个 DVB-S 发射机](http://panteltje.com/panteltje/raspberry_pi_dvb-s_transmitter/)。DVB-S 是最初为卫星广播创建的电视传输标准，但业余爱好者也用它来发送视频。[Jan]所做的是使用 Pi 上的软件将视频编码到传输流中，然后传输到自制的发射器，发射器将数据调制成 DVB-S 信号。[Jan]成功测试了直接连接的系统，将发射机的输出馈入 DVB-S 解码卡，该卡可以读取数据并解码视频信号。为了产生真正的广播信号，下一步是将信号输出馈入广播信号的放大器和更大的发射机。

不过，这是一个很大的进步，我希望[Jan]先做更多的文档。目前，这方面的示意图都是手绘的，原型是一个用电线包裹的原型板。这是一个非常令人印象深刻的黑客行为:有[个业余 DVB-S 发射机可用](http://datv-express.com/)，但大多数都将编码放在一个专用芯片上。在之前，我们已经看到黑客使用[更简单的 DVB-T 标准和 Pi，但是让 Pi 来做一些繁重的工作会使它更便宜和更灵活，所以对[Jan]和同事们的工作表示敬意。](http://hackaday.com/2015/03/28/transmitting-hd-video-from-a-raspberry-pi/)

![cabling](img/2d6d843fc39dea4068f6a3dcac8dec60.png)