# 树莓 Pi 假期家庭自动化

> 原文：<https://hackaday.com/2017/01/13/raspberry-pi-home-automation-for-the-holidays/>

当你想尝试一项新技术时，你会直接跳到生产机械吗？没有。作为概念证明，没有什么比简化模型更好的了。唯一比好的概念证明更好的是有趣的概念证明。本着这种精神，[Eric Tsai]，别名[electronichamsters]，在今年圣诞节建造了世界上最复杂的[电子姜饼屋](http://www.instructables.com/id/Magic-Gingerbread-House/)，因为家庭自动化姜饼屋仍然比家庭自动化房屋简单。

[![fya59blixaq00y3-large](img/6ffef4ee016908a32a869cddde293c78.png)](https://hackaday.com/wp-content/uploads/2017/01/fya59blixaq00y3-large.jpg) 是的，有闪闪发光的灯，这一切都是由他的智能手机控制的。这只是最基本的。然而，演示的关键是他一路构建的蓝牙到 MQTT 网关。一个带有 BTLE 无线电的树莓 Pi 接收来自 BTLE 传感器的本地数据，并将它们推送到 MQTT 服务器，原则上它们可以在世界上的任何地方被读取。如果你尝试过网络电池供电的 ESP8266 节点，你知道电池寿命是致命的弱点。切换到 BTLE 的无线电层很有意义。

如果你认为你以前见过这个，也许你会想到[电子大师]以前的家庭自动化和纸板的壮举，这也很有趣。如果以“物联网”和“仓鼠”为关键词的网络搜索让你来到这里: [Hackaday 旨在取悦](http://hackaday.com/2016/05/03/not-even-hamsters-are-safe-from-the-internet-of-things/)。

 [https://www.youtube.com/embed/5QengjRO6EM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/5QengjRO6EM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

