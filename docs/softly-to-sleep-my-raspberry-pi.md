# 轻轻地睡吧，我的覆盆子

> 原文：<https://hackaday.com/2017/07/04/softly-to-sleep-my-raspberry-pi/>

对于它们的所有容量，关闭树莓 Pi 可能是一个令人烦恼的例行程序，这取决于你如何设置它——历史上突然断电有损坏 SD 卡的风险。[madlab5]必须对无头模式下运行的 Pi 进行一些更改，要求他们从外部访问它以将其关闭，以防止拔出插头造成任何损坏。那么，为什么不抓住这个机会快速启动一个[软关机开关](http://madlab5.blogspot.ca/2017/06/adding-soft-shutdown-switch-to-headless.html)？

这是一个很好的初学者项目，可以让你习惯于使用 Pi。考虑到这一点，[madlab5]对这个想法进行了两次修改:简单的方式和有趣的方式。最简单的方法就是按下按钮，Pi 会激活一个脚本，这个脚本会在 30 秒内关闭它。任务完成。但是，意识到在某些情况下他们可能需要更多的功能，[madlab5]决定再次尝试。

[madlab5]的有趣方式包括一个内置 LED 的按钮和一个扬声器，以嘟嘟声宣布 Pi 将在短时间内自毁关闭。以这种方式设置开关需要做更多的工作，但是您可以使用自定义的关机报告为您的 Pi 添加更多的字符，以及取消意外按键的选项。

对于任何新手来说，[madlab5]在他们的博客文章中提供了他们的代码和图表。如果你更喜欢遥控器，我们也有一个类似的初学者项目来关闭你的 Pi。

[via[/r/Raspberry _ Pi _ Projects](https://www.reddit.com/r/RASPBERRY_PI_PROJECTS/comments/6jmmkq/building_a_soft_shutdown_switch_for_raspberry_pi/)