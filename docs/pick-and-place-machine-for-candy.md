# 糖果取放机

> 原文：<https://hackaday.com/2016/12/29/pick-and-place-machine-for-candy/>

每年 12 月和 5 月，来自工程学院的高级设计项目开始蜂拥而至。由于学生们还没有被现实世界中的诽谤者(比如管理层)所困扰，这些项目通常都是异常的、独特的，并且解决了我们从未想过的问题。[Mark]和[Peter]的高级设计项目就是如此:[一种承诺解决所有生活问题的取放机器](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/pas324_ml634/pas324_ml634/pas324_ml634/index.html)。

当然，我们以前见过拾放机，但这一台不同。这台机器能够识别和分类糖果，而不是识别设置在 PCB 上的电阻和电容。这个机器人——手臂的一个版本——有三个自由度和一个计算机视觉系统来提醒手臂它拿起了什么，应该放在哪里。Raspberry Pi 处理计算机视觉，并将数据输入与硬件接口的 PIC32。

高级设计课程的要求之一是将预算控制在 100 美元以下，他们可以尽可能使用预构建的解决方案来实现这一点。具有可靠精度的机器人手臂甚至无法接近这个价格限制。但是这个项目通过使用增量校正步骤来达到适当的对准，从而克服了 MeArm 中精度的不足。这在下面的视频演示中有所涉及。

高级设计课是教学生如何将他们所有的知识整合到最终课程中的一个很好的方式，教授们通常会包括他们在现实世界中可能会发现的限制(就像这个项目中的预算限制)。彻底记录构建过程的需求也是更多人应该学习的一课。高级设计班也试图解决许多生活中的其他问题；从[自动驾驶汽车](http://hackaday.com/2015/02/01/autonomous-vehicle-following-vehicle/)到[调酒师](http://hackaday.com/2015/04/26/senior-design-project-serves-infinite-drinks/)，几乎每个问题都有解决方案。

 [https://www.youtube.com/embed/oAdOXSS1_x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oAdOXSS1_x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

