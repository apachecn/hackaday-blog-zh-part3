# Minions 将您的键盘变成蓝牙键盘

> 原文：<https://hackaday.com/2016/04/14/minions-turn-your-keyboard-into-a-bluetooth-keyboard/>

邪恶的天才通常有一些匿名的追随者或其他帮凶的帮助，但对我们其他人来说，这些资源通常是遥不可及的。另一方面，[Evan]正在走向一个乐于助人的奴才大军，他们会听从他的命令:他最近开发了一个 [USB 驱动的奴才，可以将普通的 PS/2 鼠标和键盘变成蓝牙鼠标和键盘](https://www.youtube.com/watch?v=UJaqHnPR-XE)。

[Evan]在一家麦当劳找到了他的仆人，把里面所有的东西都拿了出来，把他的仆人当作所有有趣的东西的盒子。首先，他从一个旧主板上清理出一个 PS/2 端口。Arduino Nano 连接到 HC-05 蓝牙芯片，将来自 PS/2 外设的信号转换为蓝牙信号。HC-05 芯片是大多数其他蓝牙芯片的廉价替代品，价格约为 3 美元，而传统芯片的价格为 40 美元。这里的编程值得一提:[Evan]为他开源的 Arduino 编写了一个基于非中断和非阻塞的 PS/2 库，这是该项目的真正瑰宝。

一旦所有的布线和编程完成，[埃文]可以把任何旧键盘和鼠标变成可以在任何现代设备上工作的东西。他还在这个小家伙的头上放了一个 NFC 标签，这样他要连接键盘和鼠标所要做的就是将他的平板电脑或手机刷过这个小家伙。

如果你正在为你的下一个项目寻找一个有趣的案例，这个麦当劳的迷你玩具[似乎非常受欢迎](http://hackaday.com/2013/08/23/hacking-mcdonalds-minion-toy-to-be-an-electric-slidewhistle/)。PS/2 键盘显然仍然无处不在，尽管它们由于 USB 而过时了。但是还有很多其他的方法可以更好的利用这些资源。

 [https://www.youtube.com/embed/UJaqHnPR-XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UJaqHnPR-XE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

