# 非常聪明的 555 低音合成器/音序器

> 原文：<https://hackaday.com/2016/06/18/very-clever-555-bassline-synthsequencer/>

如果我们看到的每一个基于 555 的噪声制造电路都有一毛钱的话…但是这个有一个转折。

[特里斯坦]做了两件事，使他的锯齿波噪声器高于正常水平。首先，他得到了一个清晰的锯齿波，这样听起来就差不多了。然后他设法让它或多或少可以玩。这是经典黑客技术的改良版。

[![555sawtoothosc2](img/85e7794d790ac7291862c92ae3783c24.png)](https://hackaday.com/wp-content/uploads/2016/06/555sawtoothosc2.png)

第一个技巧是在定时电容的上游放置一个恒定电流源。通常的 555 定时器电路只是通过一个电阻从电源轨给电容充电。如果你只关心时机，这没问题。但是因为电流与不断下降的电压差成比例，所以电容器上的电压是随时间的[指数函数。](http://hyperphysics.phy-astr.gsu.edu/hbase/electric/capchg.html)

一个简单的晶体管电流源立即使波形线性化。原始锯齿波“谐波丰富”，这是 synth-geek 对“一点光栅”的代码，但它肯定会做得很好[加上一点滤波](https://tristandabbles.wordpress.com/2011/06/15/the-steiner-resonant-filter-a-new-adaptation)。Javascript 表明他已经朝那个方向思考了，但是我们需要视频证明！

[特里斯坦]的第二个妙招是决定音高的光敏电阻(LDR)。是的，我们以前都做过这些——依赖光线的“特雷门琴”。但是[特里斯坦]采取了额外的步骤，编写了一个 Javascript 应用程序，使他的显示器变得更亮更暗，使他能够从这个小发明中获得音乐音高。

在写[逻辑噪声](http://hackaday.com/?s=logic+noise)系列的时候，我们一直想实现 LED 到 LDR 的控制，但是一直没有找到一个可靠的方法让它工作。看到[特里斯坦]的努力很酷。也许为了纪念他，我们会从垃圾箱里拿出一辆[555](http://hackaday.com/2016/02/23/555-teardown-and-analysis/)。