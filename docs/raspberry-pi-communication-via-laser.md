# 通过激光进行树莓 Pi 通信

> 原文：<https://hackaday.com/2015/12/12/raspberry-pi-communication-via-laser/>

[Nick Touran]想让两个树莓派进行无线通信。有很多选择，但是[尼克]使用了一个[激光器和一个光敏电阻，以及莫尔斯电码](http://www.partofthething.com/thoughts/?p=835)。如果你觉得莫尔斯电码不够奇特，你可以把它称为 OOK(开/关键控)。该电路使用一个普通的激光模块和一个普通的光敏电阻，光敏电阻的电阻根据光线而变化。一个电阻与光敏电阻形成一个分压器，外部 A/D 读取产生的电压。

电路工作，但我们不禁注意到几个项目。不是所有的光敏电阻对相同的光波长都很敏感，所以为了达到最大范围，你需要选择一个特定的光敏电阻。虽然模数转换器肯定是可行的，但我们不禁想知道，是否可以设置分压器，将 Raspberry Pi 输入引脚的固有阈值用于更简单的电路。当然，如果你在 Arduino 上使用相同的技术，你可以使用内置的 A/D 转换器，A/D 转换器可能更容易工作。

原型只使用一个 Pi 与自己对话，但是如果有两个，它们可以使用这种方案相互对话。该软件使用一些以前[Nick]编写的代码来生成代码，看起来很容易使用和修改。

用光交流并不是一个新想法。[贝尔有光电话](http://hackaday.com/2011/06/03/dino-celebrates-the-131st-anniversary-of-the-photophone/)，我们在之前已经报道过[激光通信。就在昨天，我们](http://hackaday.com/2015/07/02/solar-cell-laser-communication-system/)[在 LiFi](http://hackaday.com/2015/12/11/hackaday-explains-li-fi-visible-light-communications/) 上发表了一篇文章，试图用光取代 WiFi。