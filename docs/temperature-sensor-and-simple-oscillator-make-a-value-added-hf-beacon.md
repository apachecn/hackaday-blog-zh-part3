# 温度传感器和简单的振荡器构成了一个增值的高频信标

> 原文：<https://hackaday.com/2018/04/24/temperature-sensor-and-simple-oscillator-make-a-value-added-hf-beacon/>

有时最好的项目是简单、快速的点击。设计简单，构建快速，第一次就能正确工作的奖励积分。这样的项目通常会带来更大更好的东西，这似乎是这个低功耗温度灯塔的方向。

在业余无线电领域，信标站是一种发射机，通常在已知位置无人值守运行，通常处于[有限功率(QRP)](http://hackaday.com/2016/03/08/how-low-can-you-go-the-world-of-qrp-operation/) 。大多数信标旨在供其他 hams 用来确定传播条件，只是发送运营商的呼号，有时会以不同的功率水平发送。任何可以接收信号的 ham 都知道信标和接收器之间有一条传播路径，这有助于建立联系。[戴夫·理查兹(AA7EE)]建造的信标不是火腿信标，至少现在还不是；它工作在 13.56 MHz，利用了 FCC Part 15 关于低功率传输的规定，而不是 Part 97 关于业余无线电的规定。电路非常简单，一个单晶体管科尔皮兹振荡器，没有功率放大器，因此范围非常有限。但作为一个额外的变化，振荡器由一个与 LM335 温度传感器相连的 ATtiny13 控制，大约每 30 秒钟用莫尔斯电码发送一次摄氏和华氏温度。这条赛道以[曼哈顿风格](http://hackaday.com/2016/05/04/getting-ugly-dead-bugs-and-going-to-manhattan/)执行，看起来很棒，并留有足够的扩展空间。[Dave]提到添加一个功率放大器和一个低通滤波器来消除谐波，并使其在 ham 频段中合法。

信标只是火腿们不说话就开始广播的方式之一。另一种分析传播的有趣方式是 [WSPR](http://hackaday.com/2013/03/21/wspr-transmitter-shows-true-value-of-raspberry-pi-for-hacking/) ，它有点像物联网信标。

 [https://www.youtube.com/embed/GoqZsD6_gcQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GoqZsD6_gcQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [危险原型](http://dangerousprototypes.com/blog/2018/04/23/the-k7tmg-hf-morse-code-temperature-beacon/)