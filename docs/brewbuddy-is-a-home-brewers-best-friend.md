# BrewBuddy 是家庭酿酒商最好的朋友

> 原文：<https://hackaday.com/2018/01/08/brewbuddy-is-a-home-brewers-best-friend/>

无论你喜欢咖啡、茶还是啤酒，冲泡都是时间和温度的微妙的双人舞。这些饮料中的任何一种的适当酿造都可以将体验从一般提升到惊人。考虑到这一点，[Marcelo]创造了一个时间和温度工具，以调整他的啤酒酿造过程。

[BrewBuddy 是一款复杂的专用定时器，内置温度计](https://hackaday.io/project/28667-brewbuddy)。它可以让他为捣碎过程和煮沸过程设定时间和温度曲线，并为每个过程存储多达 10 个步骤。BrewBuddy 不控制酿造温度，但它将温度测量和时间标记统一到一个方便的设备中，可以在单个 CR2032 上持续约 20 小时。

该系统基于一个 STM32 和一个 LMT86 模拟温度传感器，该传感器已被修改为位于一个不锈钢管内。有四个方向按钮可以通过直观的菜单来设置所需的时间和温度。每个步骤完成后，状态 LED 灯亮起，BrewBuddy 等待按钮确认，然后进入下一步。如果有问题，可以使用向上/向下按钮暂停和恢复计时器。[Marcelo]正在努力完善机箱设计，但他已经在 GitHub 上发布了[电路板文件和固件](https://github.com/marcelobarrosalmeida/brewbuddy)。打开一个冷的，休息后看看演示视频。

煮沸和冷却后是发酵，这需要仔细监控含糖量。这里有一个工具。

 [https://www.youtube.com/embed/FMSUGOILIN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FMSUGOILIN4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/00Js_LpAEr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/00Js_LpAEr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Coin Cell ChallengeBuild something cool powered
by a coin cell, win prizes![Enter now](https://hackaday.io/contest/28283-coin-cell-challenge)[See all entries](https://hackaday.io/submissions/coin-cell-challenge/list)