# 无线电干扰步枪声称能摧毁无人机

> 原文：<https://hackaday.com/2015/10/24/radio-jamming-rifle-claimed-to-disable-drones/>

总部位于俄亥俄州的非营利 R&D 公司[Battelle]刚刚推出了一种他们称为 [DroneDefender](http://www.battelle.org/media/press-releases/rogue-drones-have-met-their-match) 的设备——一种远程反无人机防御武器。这听起来就像他们把虚构的[无人机猎人的射频加农炮](http://hackaday.com/2014/10/29/from-nerf-gun-to-rf-cannon-building-a-movie-prop/)变成了现实。但是真的管用吗？

据该网站称，它使用无线电频率干扰将多余的无人机从天空中炸出。很酷的概念，但它真的有用吗？与 Parrot AR、ArduPilot 和少数其他消费无人机使用的[可黑客攻击的 MAVLink 协议](http://hackaday.com/2015/10/15/hijacking-quadcopters-with-a-mavlink-exploit/)不同，这种武器使用暴力无线电信号力量来禁用任何(？)消费级无人机。

休息之后有一段视频演示了该技术的模拟使用，这让我们有点困惑。他们展示了无人机在步枪的“引导”下缓缓降落。如果系统同时干扰 GPS 和 2.4 GHz 控制链路，行为将完全取决于无人机上装载的软件。一些将进入故障安全模式，即低油门或马达断电，假设飞行员设置了故障安全。其他人可能试图仅在 IMU 传感器上游荡。

 [https://www.youtube.com/embed/zX4XXLb_Vuw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zX4XXLb_Vuw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



根据[Battelle]的说法——该系统实际上在现场测试场景中工作，但由于美国联邦法规，他们不能炫耀它。

我们想知道的是，如果真的像用无线电信号轰炸无人机这么简单，为什么黑客社区还没有人去做？把它当成一个挑战吧——把你的进步发布到 [Hackaday.io 上！](https://hackaday.io/)

[via [BGR](http://bgr.com/2015/10/16/drone-defender-rifle-radio-wave-gun/) ，感谢保罗的提示！]