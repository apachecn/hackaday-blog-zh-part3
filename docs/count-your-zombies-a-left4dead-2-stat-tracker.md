# 数数你的僵尸！Left4Dead 2 Stat 追踪器

> 原文：<https://hackaday.com/2017/03/17/count-your-zombies-a-left4dead-2-stat-tracker/>

当然，你越来越深入游戏并完成任务，但僵尸射手的真正进步是你杀死了多少僵尸，对吗？[Evan Juras]同意了，于是他着手为 Left4Dead 2 打造硬件 [stat 追踪器！](https://hackaday.io/project/19785-left-4-dead-2-stat-tracker)

Left4Dead 2 会追踪一系列统计数据，在每一关结束时，这些数据会在你的 Steam 页面上更新。[Evan]使用运行在 Raspberry Pi 上的 Python 脚本连接到互联网，并从您的 Steam 个人资料中获取四种不同的统计数据。这些统计数据显示在 RGB 16×2 显示器上。为了容纳这个项目，我们为它设计了一个盒子，然后[埃文]用 3D 打印了它。机箱上有两个按钮:一个用于更新统计数据，另一个用于循环显示。如果没有按下任何按钮，则显示每分钟循环一次统计数据，并每 24 小时更新一次统计数据。

下面的视频显示了构建过程的摘要，并描述了所使用的硬件和软件。[Evan]计划通过 Steam 跟踪其他游戏的统计数据，他的 python 代码可在 Github 上获得。Python 正在成为与视频游戏机器人互动的首选工具，现在，stats 见 Pokemon Go 机器人列表。此外，如果你想在没有 Raspberry Pi 的情况下构建类似的东西，请查看关于在 ESP8266 上运行 MicroPython 的[特性](http://hackaday.com/2016/07/21/micropython-on-the-esp8266-kicking-the-tires/)。

 [https://www.youtube.com/embed/8G3mvy-2taM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8G3mvy-2taM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

