# 内置 3G 的计算器

> 原文：<https://hackaday.com/2017/12/24/a-calculator-with-3g-inside/>

对于我们许多人来说，计算器是我们在手机上运行的一个应用程序。甚至几十年前的功能手机也捆绑了某种形式的计算器，因此这种特定的任务已经加入了功能到一个设备中的不可避免的融合。

然而对于斯科特·豪伊来说，手机是一个可以在他的计算器上运行的应用程序。他在 TI-84 计算器中集成了一个手机模块，虽然它可能还不会把苹果或三星赶下神坛，但它功能齐全，既能打电话也能接电话。

为了实现这一壮举，他拿起手机模块和一块最小的 Arduino 板，通过尽可能多地去除多余的塑料，将它们安装在 TI-84 键盘下方的空间中。计算器的 4 节 AAA 电池自身无法提供足够的电力，所以他补充了几节电池，并用可充电电池取代了碱性电池。一个隐藏的开关可以让手机关机以延长电池寿命。

计算器通过一根有点难看的外部串行电缆与 Arduino 对话，[他所有的软件都可以在 GitHub 库中方便地获得](https://github.com/BoomBrush/Calcucall)。他的视频详细展示了整个构建过程，所以如果你喜欢一个带蜂窝连接的计算器，这就是你的机会。等等，难道你不能用这样的设备来作弊吗？

 [https://www.youtube.com/embed/XhAPQs9kyEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XhAPQs9kyEw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



据我们所知，这仍然是我们带给你的唯一的计算器/手机组合，尽管我们已经在计算器上看到了 [Android。与此同时，其他计算器也出现在这里，如](https://hackaday.com/2015/06/26/android-donut-running-on-a-graphing-calculator/)[这个拆了一个经典的 Sinclair](https://hackaday.com/2017/11/01/a-teardown-with-a-twist-1975-sinclair-scientific-calculator/) 。