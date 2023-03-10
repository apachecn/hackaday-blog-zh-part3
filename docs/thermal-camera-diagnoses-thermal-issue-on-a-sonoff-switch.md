# 热感摄像机诊断 Sonoff 开关的温度问题

> 原文：<https://hackaday.com/2018/03/03/thermal-camera-diagnoses-thermal-issue-on-a-sonoff-switch/>

无论您的故障诊断经验水平如何，当您不得不开始查看电源供电设备时，总会有一点担心。有点恐惧是好事；它让你保持专注。然而，对于一些人来说，厌恶玩高压太多了，这可能会在某个东西出现故障时引发问题。那么当你甚至不愿意打开箱子的时候你会怎么做呢？简单— [用红外摄像机](https://www.baldengineer.com/debug-sonoff-ac-relay-thermal-camera.html)诊断问题。

[![](img/550659ae805d4035baf094191090de07.png)](https://hackaday.com/wp-content/uploads/2018/02/thermal-runaway-corrected.gif) 【光头工程师】的电恐惧症很早就开始了，在经皮传导方面做了一些欠考虑的实验。因此，当他的新 Sonoff WiFi 开关在部署后不久就无法控制他工作室的灯时，在它通电时弹出顶部是不可能的。热塑料的辛辣气味是他解决问题的第一个线索，所以他拿出他的 [Flir One 热感相机](https://hackaday.com/2016/04/20/hackaday-reviews-flir-one-android/)，看着设备通电。附近的 GIF 显示，显然存在问题，热量从设备中心迅速扩散。顶部和底部的一些红外图像给了他一些关于罪犯的线索，但在断电后探测这些区域的电路板并没有发现明显损坏的组件。

[秃头工程师]还没有弄清楚这一点，但他目前的想法是，NCP1117 调节器可能是坏的，因为它迅速飙升至 115°c。尽管如此，我们认为这是一种可以添加到我们的工具包中的漂亮的诊断技术，也是一个购买红外相机的好借口。或者，我们可以用[开源热感相机](https://hackaday.com/2017/02/08/diy-thermal-camera-thats-better-and-cheaper-than-a-flir/)来代替。

[via [危险原型](http://dangerousprototypes.com/blog/2018/02/27/debug-sonoff-ac-relay-with-a-thermal-camera/)