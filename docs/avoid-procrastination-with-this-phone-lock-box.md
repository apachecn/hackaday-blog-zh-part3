# 使用这个手机锁盒避免拖延

> 原文：<https://hackaday.com/2015/11/12/avoid-procrastination-with-this-phone-lock-box/>

智能手机很棒。如此之大，以至于你可能会发现自己无法专心工作、吃饭、与人交谈，甚至睡觉。[Digitaljunky]有这个问题(考虑到他的名字，真的不奇怪)，所以他做了一个反拖延盒子。这个盒子足够大，可以容纳一部智能手机，并且有一个基于 Arduino 的时间锁。

真正的诀窍是制作盒子，以便 Arduino 可以用螺线管锁定和解锁它。[Digitaljunky]没有 3D 打印机，所以他用 Fimo 粘土塑造了一个定制的插销片。一个数字显示器，一个 FET 来驱动螺线管，以及一些常见的组件完善了设计。

该软件使用 C++类来组织一切。你可以[在 Github](https://github.com/amatelin/arduino-code-repo/tree/master/safe_box/SafeBox/Main/Main) 上下载代码。使用方法很简单(见下面的视频)。当你等待 Arduino 打开盒子的时候，把你的手机锁起来，做一些工作。

我们认为使用粘土而不是传统的 3D 打印部件可以更容易地复制该项目。当然，你可以 3D 打印一件作品，如果你真的想融合两个世界，你总是可以用粘土 3D 打印。当然，如果你想要一个更简单的解决方案，你可以只为手机编写锁定软件。另一方面，这个盒子可以锁住任何诱人的东西，不仅仅是一部手机。

 [https://www.youtube.com/embed/aSoCY1dWrtE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aSoCY1dWrtE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

