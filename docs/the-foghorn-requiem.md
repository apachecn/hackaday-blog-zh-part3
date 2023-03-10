# 雾号安魂曲

> 原文：<https://hackaday.com/2016/05/30/the-foghorn-requiem/>

自 19 世纪以来，雾号一直是航海历史的一部分，在恶劣天气下为出海的水手提供急需的安全保障。随着时间的推移，它们的相关性慢慢降低，先进的导航设备接管了保护船只和水手安全的任务。

雾号的声音正在慢慢消失。艺术家[Joshua Portway]和[Lise Autogena]共同创作了[Foghorn 安魂曲](http://foghornrequiem.org/)，该项目于 2013 年 6 月 22 日^和达到高潮，一支由 50 多艘船只组成的舰队聚集在北海上演奏了一首雄心勃勃的音乐，标志着 fog horn 的声音从英国的沿海景观中消失。

近距离观察，雾号的声音足以把你的鞋子震掉。但经过一段距离，它的声音呈现出一种深情、忧郁的特质，这是由它所经过的地形决定的。在作曲家奥兰多·高夫(Orlando Gough)的帮助下，艺术家们试图捕捉雾号的这种品质，他为这场演出创作了一个特别的配乐。它汇集了三个铜管乐队——the Felling 乐队、Westoe 乐队和 NASUWT Riverside 乐队，近 50 艘海上船只和 Souter Lighthouse Foghorn 来演奏乐谱。

 [![horn_preparation](img/786d2096f3234a0b109813ba24ab5aa7.png "horn_preparation")](https://hackaday.com/2016/05/30/the-foghorn-requiem/horn_preparation/)  [![foghorn_controller](img/2c4a0ae7163f682ade32751499ab226c.png "foghorn_controller")](https://hackaday.com/2016/05/30/the-foghorn-requiem/foghorn_controller/) 

50 多艘船只中的每一艘都配备了定制的可调雾号，由控制器盒驱动，控制器盒由 TI 发射台组成，带有 GPS、RTC、Xbee 无线电和中继模块。由于船只和陆地上的观众之间的距离很远，这些设备需要补偿它们的相对位置，并调整它们播放雾号的时间，以抵消声音的传播时间。每个控制器都将其特定分数保存在板载存储器中，所有控制器都与一个公共实时时钟同步。

从表演开始大约 10 分钟后，海事无线电被用来与所有船只联系，通知他们何时打开控制器。然后，每个设备使用其 GPS 位置来计算其与预先编程的观众位置的距离，并计算出它必须提前多少秒钟按喇叭，才能在岸上及时听到声音。然后，控制器等待预编程的时间，开始播放他们各自的雾号音符。这个想法很酷的一点是不需要交流——一切都基于时间。休息之后，看看《雾号安魂曲》的制作视频，这里有一个链接，链接到最后演出的[音轨](http://foghornrequiem.org/listen)。

与我们之前发布的[超级大型乐器](http://hackaday.com/2016/05/07/super-massive-musical-instrument/)相比，这是一个稍微不同的方法。

[https://player.vimeo.com/video/119231430](https://player.vimeo.com/video/119231430)