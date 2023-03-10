# 烘干机完成后会发短信给你

> 原文：<https://hackaday.com/2017/12/09/finished-dryer-will-text-you/>

这里有一个稍微不同的方法来检查你的衣服的状态。不是检查机器是否在振动，或者听声音，或者把所有东西都拆开，然后把 ESP8266 插进去，而是检查机器消耗的功率。这就是 Scrand 在他的物联网烘干机中所做的。

黑客背后的秘密是 Sonoff POW，一种位于墙壁和烘干机之间的小设备。它有一个控制它的继电器，但是，对这个黑客来说重要的是，它能够测量插入它的东西所使用的功耗。通过在上面安装 [ESPurna](https://bitbucket.org/xoseperez/espurna) 固件，他现在可以使用固件的所有功能来控制和监控连接到电源的设备。他编写了一个 PowerShell 脚本来监控现在运行在 POW 上的 http 服务器，检查烘干机消耗了多少功率。当电量下降时，衣服就洗好了，而在[Scrand]的情况下，会发送一条短信来说明这一点。

当你坐在沙发上放松的时候，为什么要每五分钟起来检查一下你要洗的衣服，当你知道洗好了的时候，它会给你发短信。然后你可以决定是起床去处理它还是把它留到以后。ESPurna 存在的全部原因是为了[检查洗衣房的状态](https://hackaday.com/2016/08/01/your-laundry-is-done/)。或者，你可以用[这个洗衣房监视器](https://hackaday.com/2017/02/18/monitor-all-the-laundry-things-with-this-sleek-iot-system/)来做得有点过火。