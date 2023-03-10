# 用树莓皮凭空变出音乐

> 原文：<https://hackaday.com/2018/02/15/pulling-music-out-of-thin-air-with-a-raspberry-pi/>

钢琴是很好的乐器，但是相当重，需要相当大的空间，它们当然不方便。当然，有更多的便携式品种可供选择，但它们很少像三角钢琴那样优雅和高雅。一个选择当然是自己制作一个缩小版——既然你已经定制了乐器，为什么还要停留在你演奏的方式上。[2fishy]也没有就此止步，最终得到了一架木制的、对空间友好的光控钢琴,里面有一个树莓派。

受激光竖琴概念的启发，[2fishy]遵循了同样的原则，但选择了更简单、更安全的替代方案，使用 led。对于每个可播放的音调，LED 安装在光敏电阻的对面，创建一个开关阵列，然后连接到 Raspberry Pi 的 GPIO 引脚。Python 脚本处理剩下的事情，轮询 GPIO 状态，并在 [pygame](https://www.pygame.org/) 的帮助下，每当光流中断时触发 MIDI 播放。

有足够的 LED/LDR 对播放一个完整的八度音阶，并有一些额外的菜单和八度音阶转换控制输入。这个概念自然需要对你的演奏进行一些调整——你可以在休息后的演示视频中了解它。如果这种设计仍然不适合你，或者如果你喜欢在完全黑暗的环境中演奏，[这种类似的使用超声波距离传感器的 MIDI 乐器](https://hackaday.com/2017/04/22/ultrasonic-raspberry-pi-piano/)可能会让你感兴趣。

 [https://www.youtube.com/embed/mKOGDsw6MME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mKOGDsw6MME?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

