# 朋友学校对鲨鱼使用思想控制

> 原文：<https://hackaday.com/2015/09/26/school-of-friends-use-thought-control-on-a-shark/>

[Chip Audette]拥有(至少)两个小工具:一个是遥控充氦飞行鲨鱼(一个空中游泳者)，一个是 OpenBCI 脑电图系统，可以读取脑电波，并将数据输入电脑。有了这些信息，你就不会惊讶于[Chip] [决定用他的大脑](http://spectrum.ieee.org/geek-life/hands-on/openbci-control-an-air-shark-with-your-mind)控制他的飞鱼。

在你变得过于兴奋之前，你必须(比如[Chip])改变你的预期。虽然脑电图有很多信息，但你的直接想法(可能)是不可读的。然而，某些动作会在 EEG 数据中创建易于识别的模式。特别是，闭上眼睛会在后脑勺产生强烈的 10Hz 信号。

为了控制这条鱼，[Chip]用 Arduino 连接了股票遥控器。问题是，虽然遥控器有五种不同的动作，但[芯片]只能很容易地检测到眼睛是闭着的。OpenBCI 可以让你在不同的频道上读取不同人的脑电图，所以[芯片]连接了四个朋友，现在需要五个人才能完全控制大白鲨的兄弟。

在之前，我们已经[讨论过 OpenBCI 以及另一个脑电图设备的](http://hackaday.com/2015/03/17/brains-controlling-labyrinths-without-hands/)[拆除，Muse 耳机](http://hackaday.com/2015/07/15/muse-eeg-headset-teardown/)。我们只是希望[Chip]为明显的“跳过鲨鱼”评论做好准备。

 [https://www.youtube.com/embed/Qnr3YWWAZL0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Qnr3YWWAZL0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

