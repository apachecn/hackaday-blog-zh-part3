# Alexa 机器人咖啡机冲泡咖啡，不言自明

> 原文：<https://hackaday.com/2017/01/06/alexa-robot-coffee-maker-brews-coffee-speaks-for-itself/>

为了让黑客们继续攻击，为什么不把咖啡机改装成咖啡冲泡机器人呢？[卡特·赫德]和[大卫·弗兰克]在俄亥俄州的黑客 OHI/24 小时黑客马拉松上就是这样做的。他们甚至获得了“最佳硬件黑客”。下面的视频展示了它的工作过程，但是他们给了我们一些额外的细节。

 [![Alexa coffee maker robot](img/d126774671bd4e751a46ff3178138a64.png "Alexa coffee maker robot")](https://hackaday.com/2017/01/06/alexa-robot-coffee-maker-brews-coffee-speaks-for-itself/alexa_coffee_maker_fullsizerender/) Alexa coffee maker robot [![The electronics for the Alexa coffee maker robot](img/588cfbf25619739f7245f77b47578e2c.png "The electronics")](https://hackaday.com/2017/01/06/alexa-robot-coffee-maker-brews-coffee-speaks-for-itself/alexa_coffee_maker_fullsizerender-4/) The electronics

为了给它一个声音，他们把 Alexa 放在树莓皮上。使用音频分离器，他们可以将声音传送到扬声器和 Arduino。Arduino 然后使用音频信号正值的幅度来确定“嘴”(咖啡机的铰链盖)打开的程度。通常情况下，会有一些滞后，但结果仍然很好。

酿造也由 Arduino 控制。他们计划添加语音控制，这样他们就可以简单地问，“Alexa，给我煮咖啡”，但现在他们在旁边添加了一个开关来开始冲泡。这个开关告诉 Arduino 使用一个伺服系统打开盖子，另一个伺服系统插入咖啡过滤器，还有两个伺服系统从容器中舀取一些咖啡并倒入过滤器。

他们用继电器取代了咖啡机的开/关开关，这样在 Arduino 再次合上盖子后，它就会使用继电器开始冲泡。结果出奇的像人类。我们尤其喜欢两个伺服机构舀起和倾倒咖啡的优雅动作。完全披露:他们确实承认，通常不是舀得不够多，就是舀得不够多，却洒了一大堆在小组成员身上。

[卡特]和[大卫]从 Alexa 控制的大嘴巴 Billy Bass 那里获得了他们咖啡机的灵感。但是，如果你正在寻找一个能够煮出一杯完美咖啡的咖啡机[黑客，那么看看这里就够了。](http://hackaday.com/2013/02/14/hacking-a-coffee-machine-for-a-better-brew/)

 [https://www.youtube.com/embed/dH_PcpzAIy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dH_PcpzAIy4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

