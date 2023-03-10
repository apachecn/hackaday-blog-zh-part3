# 一个人寻求减少在地下室的时间

> 原文：<https://hackaday.com/2016/03/12/one-mans-quest-to-spend-less-time-in-the-basement/>

[拉斯]有一个二楼公寓，洗衣机和干衣机在地下室。这意味着[Lars]花了太多的时间走到地下室去取他要洗的衣服，却发现这个周期还剩 15 分钟。有几个解决方案:像一只不体贴的动物一样把你的衣物放在洗衣机里，买一个新的、别致的、带有专有物联网软件的洗衣机和干衣机，或者一起组装一个洗衣机和干衣机监控解决方案。[我们都知道【Lars】选择了什么选项](https://hackaday.io/project/9432-monitoring-washing-machines)。

将 Pi 连接到互联网并提供少量数据是一个已解决的问题。困难的部分是决定服务哪些位。洗衣机和烘干机都有一些共同点:它们都使用电力，它们都移动和震动，它们发出噪音，它们的界面在洗涤周期中会发生变化。[Lars]想要一个可以与洗衣机和烘干机一起使用的设备，并且将来可以与其他机器一起使用。他首先用麦克风进行了实验，捕捉到洗衣机晃动和烘干机翻滚衣物的低沉轰鸣声。事实证明，加速度计也能很好地工作，如果将传感器牢固地固定在洗衣机或烘干机上，[Lars]可以很好地了解它是否在运行。

通过一种可靠的方法来判断洗衣机或烘干机是否仍在运行，[Lars]只需将这些信息放到他的智能手机上。他最终使用了 PushBullet ，并很快在他的手机上安装了一个应用程序，告诉他衣服是否洗好了。

* * *

![Raspberry_Pi_LogoSmall](img/87d7e34f7ac8cc3ae6c8619ad96c149e.png)

树莓派零竞赛由 Hackaday 和 Adafruit 主办。奖品包括 Adafruit 的树莓派零和 Hackaday 商店的礼品卡！
[查看所有参赛作品](https://hackaday.io/submissions/adafruitpizerocontest/list) || [现在就进入你的项目吧！](https://hackaday.io/contest/9326-adafruit-pi-zero-contest)