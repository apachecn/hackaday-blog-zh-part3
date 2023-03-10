# 模糊的毯子隐藏着严肃的技术

> 原文：<https://hackaday.com/2016/03/20/fuzzy-blanket-hides-serious-tech/>

谁需要物联网？不是这个[互动，声音回放毯](https://knitglitch.wordpress.com/2015/10/11/blanket/)！相反，隐藏在其柔软模糊的外表下，它利用 NRF24L01+模块直接与其声音服务器通话。

这个项目是为一所学校设计的，让学生们把他们认为重要的任何声音记录到树莓派里。然后，学生们组装了物理毛毡毯子，里面缝有传感器，可以通过在地板上爬来爬去播放他们最喜欢的声音。这是一个多感官、参与性、DIY 的盛会。我们希望我们在小学也能做这样酷的事情。

[![3520911454640205800](img/87f4e1913902390cb17db72b3f26c5a5.png)](https://hackaday.com/wp-content/uploads/2016/02/3520911454640205800.png)

什么？您的“blankie”不会将数据传输到一个纯数据应用程序？嗯，[丹·麦克尼斯]在这里帮助你改变这种情况。Hackady.io 上这篇写得很好的[条目描述了他用来让毯子的多个触摸传感器通过空气发送小数据包的设置](https://hackaday.io/project/9130-embedded-puredata-wireless),[为你提供 Pd 代码，让它在 GitHub 上工作。](https://github.com/whiteboarddan/RF24-puredata)。

[![8178811454644034915](img/046639082367334afeca3e6cf61e5189.png)](https://hackaday.com/wp-content/uploads/2016/02/8178811454644034915.png) 我们非常喜欢 DIY 音乐控制器，这种简单的设置比仅仅制作毯子更有用。在这个一切都通过 WiFi 的时代，看到一个直截了当的 2.4 GHz 无线电构建是必要的，这令人耳目一新。

[Dan]抱怨 NRF24 模块只能达到 3m 左右，这让我们觉得很奇怪。也许是因为 NRF24 天线附近的所有金属？