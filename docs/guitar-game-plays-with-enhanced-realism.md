# 增强真实感的吉他游戏

> 原文：<https://hackaday.com/2017/12/13/guitar-game-plays-with-enhanced-realism/>

学习如何弹吉他不仅仅是在正确的时间以正确的顺序弹正确的音符。要发出任何声音，都需要学习如何用双手同时做完全不同的事情，除非你是艾迪·范·海伦的直系后裔，天生就会做锤子。还有一大堆其他的东西伴随着这个领域，比如把东西串起来，调好音，然后正确地储存起来，所有这些都会让新玩家感到沮丧和气馁。加上老茧，难怪人们这么喜欢吉他英雄。

[杰克]和[乔纳]已经找到了一种方法，在按糖果色按钮和长出防火老茧和足够的握力来压碎锡罐之间架起一座桥梁。[在[Bruce Land]的嵌入式微控制器设计课程的最后一个项目中，他们制作了一个吉他视频游戏和一个更接近实际弹奏吉他体验的控制器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/jhp246_jfw95/jhp246_jfw95/4760report/index.html)。无论你是学习玩真的，还是只是想玩得开心，这个游戏都是一个很好的介绍，让你了解不仅仅是制造噪音所需要的协调。

有趣的是，与标准弦乐器结构不同的是，拨弦与微动无关。演奏者用手指在四根弦上弹奏音符，但用导电拨片拨动特殊的第五根弦，闭合拨动电路。相比之下，摩擦弦通常很高。当按下时，它们接触箔覆盖的指板，电路变低。所有五根琴弦都是由碳浸渍的弹性材料制成，并且用 30AWG 铜线包裹。

所有五根线都连接到 Arduino UNO，然后连接到笔记本电脑。笔记本电脑向 Bluefruit 的朋友发送信号，将蓝牙改为 UART，以满足 PIC32。从那里，它通过 2 通道 DAC 输出到一对 PC 扬声器。一个通道有弦乐音调，由 Karplus-Strong 生成。为了填充声音，另一个 DAC 通道为每个音符传送低音，由正弦表和直接数字合成产生。没有服务费；只需点击休息时间即可查看。

如果你想开始玩，但不想花很多钱开始，不要错过那些 30-40 美元的儿童音响，甚至是玩具店 25 美元的尤克里里。你可以[给自己的皮卡上发条，然后用电动](https://hackaday.com/2016/08/03/rocking-an-acoustic-guitar-by-making-it-electric/)，或者[加上一个打击螺线管来保持节拍](https://hackaday.com/2017/12/02/modified-uke-keeps-the-beat-with-a-solenoid/)。

 [https://www.youtube.com/embed/W4QjMCd-iXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/W4QjMCd-iXQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

