# 泡泡捕手看着你的酒打嗝

> 原文：<https://hackaday.com/2015/11/24/bubble-catcher-watches-your-booze-burp/>

制作自己的酒需要坐在一旁等待事情发生，比如等待发酵过程结束，这样你就可以继续装瓶并饮用。这包括观察气闸中的气泡:一旦气泡的频率低于某一水平，你的烈酒就准备好进行下一步了。

[Waldy45]决定通过建造一个气泡捕捉器来测量气泡通过气闸的频率，从而使这一过程自动化。他使用光耦合器实现了这一点，光耦合器是 LED 和光传感器的组合，当有东西通过它们之间时，它会改变电阻。你在图像中看不到它，但马蹄形的光耦合器被开槽在气泡管中的细颈周围，以感应气泡何时通过。

光耦合器连接到 Arduino，运行一段代码，当光耦合器被触发时产生一个中断。目前，这只是将气泡之间的平均时间输出到串行端口，但[Waldy45]正在寻求添加一个 ESP8266 来无线连接 Arduino，并在气泡频率下降时联系他，这表明酒已经准备好装瓶。

我们以前见过几家顶级啤酒厂(这里的和这里的)，但它们都没有实现实际发酵阶段的自动化，所以像这样的东西肯定会是一个补充。干杯！