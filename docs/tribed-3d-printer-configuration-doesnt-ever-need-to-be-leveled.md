# Tribed 3D 打印机配置永远不需要调平

> 原文：<https://hackaday.com/2016/01/31/tribed-3d-printer-configuration-doesnt-ever-need-to-be-leveled/>

[Jeremie Francois]很长时间以来一直在思考如何在他的 [3D 打印机中改进工具高度调节和床身调平。他的梦想是永远不再考虑身高。一个](http://www.tridimake.com/2015/12/tribed-fully-automatic-bed-leveling-and-z-offset-adjustment.html)[梦](http://hackaday.com/2015/06/29/semi-automatic-bed-leveling-your-3d-printer/)那就是[被](http://hackaday.com/2014/10/05/bed-leveling-with-a-solenoid-actuator/)[多人](http://hackaday.com/2014/04/15/automated-bed-leveling-for-3d-printers-is-now-solved/)分享。如今，许多 3D 打印机的软件中都有自动调平的机制。这样做很好，但由于各种机械原因，最好让床本身保持水平。

[Jeremie]的方法相当聪明。由于你可以用三个点在数学上定义任何平面，他有三个 Z 轴丝杠。这让他可以把床倾斜到他喜欢的任何角度。一旦他有了合适的机制，他就添加了一些[力敏电阻](http://hackaday.com/2014/03/19/ask-hackaday-auto-bed-leveling-and-high-temperature-force-sensitive-resistors/)，一个 Arduino，并为流行的马林固件写了一个扩展。问题就是从那时开始的。

事实证明，将床牢固地安装在电阻上传递了太多的振动。解决方案是一层氯丁橡胶。氯丁橡胶还可以起到缓冲作用，因此在调平过程中喷嘴不会损坏玻璃床。

由于 YouTube 糟糕的自动稳定软件，休息后的视频有点波动，但如果你仔细观看，你可以看到系统在工作。

 [https://www.youtube.com/embed/_CGGhKfbbP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_CGGhKfbbP0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

