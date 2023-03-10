# 物联网鸡舍门照顾鸡，测试家庭自动化

> 原文：<https://hackaday.com/2016/11/06/iot-coop-door-cares-for-chickens-tests-home-automation/>

大多数鸡都很擅长在太阳落山时睡觉，艾迪的鸡也不例外。但是他们不太会考虑自己关门的问题，所以他开始着手一个长期项目，让他们的鸡舍门实现自动化。

整夜敞开的门会使鸡和它们的食物容易被捕食。与其手动处理这些杂务，冒着可能毁掉他的羊群的健忘时刻的风险，[Eddy]使用了一个伺服系统来给门提供动力，并使用 Arduino 来控制它。为了记录就寝时间和起床时间，树莓皮会在网上查找当地的民用黎明和黄昏时间，并告诉 Arduino 什么时候该到了。Pi 巧妙地缓存了时间，以备第二天在 WiFi 连接中断的情况下使用，还提供了一个网络界面来检查门的状态，并手动覆盖周期。结果:安全快乐的小鸡。

如果这一切对一项简单的工作来说似乎有点过了，[Eddy]同意。但他正以此为试验平台，开发一个可以随意重新分配任务的家庭自动化框架。对我们来说，听起来他的思路是正确的，但要了解更多物联网畜牧业技巧，他会想看看这个小型农场自动化项目。

 [https://www.youtube.com/embed/hlYWVG42nPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hlYWVG42nPE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

