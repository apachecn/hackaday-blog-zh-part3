# Joysix，由可伸缩钥匙圈制成的六自由度鼠标

> 原文：<https://hackaday.com/2016/02/02/joysix-six-degree-of-freedom-mouse-made-from-retractable-key-rings/>

[Nicolas Berger]提交他的[六自由度鼠标项目](https://hackaday.io/project/9354-joysix)。他希望做一些事情，比如[控制机器人手臂](http://hackaday.com/2015/07/28/3d-mouse-drives-robot-arm/)或者驾驶外星母舰。

我们认为建筑非常整洁；将一个木球悬挂在三个可伸缩的钥匙圈中间。通过移动球，你可以控制计算机上显示的立方体的运动。我们最初认为这是通过编码器或电位计测量从钥匙出来的绳子量来实现的。然而，实际上发生的事情要聪明一点。

[Nicolas]用 Adafruit 的 2 轴操纵杆连接了每根琴弦。他起初对这些有一些问题，因为操纵杆中的电位计不是线性的，但他用不同的模块替换了它们，并获得了预期的输出。他从每个字符串中获取角度值，然后一个 Python 程序将鼠标的输出数字转换成计算机喜欢的东西。代码可以在他的 GitHub 上找到。一个完整的鼠标的视频是在休息之后。

[https://player.vimeo.com/video/153554088](https://player.vimeo.com/video/153554088)