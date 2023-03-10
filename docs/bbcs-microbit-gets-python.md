# BBC 的微:比特获得 Python

> 原文：<https://hackaday.com/2015/10/20/bbcs-microbit-gets-python/>

英国广播公司开发了一台计算机，供全英国成千上万的学生使用。虽然在硬件方面不是很强大，但它带有一种解释语言，可以让学生编写自己的代码，并将开启整整一代网络开发人员的职业生涯。这当然是 BBC Micro，一台 1981 年推出的电脑，但仍深受数百万以前的学生崇敬。

现在微控制器无处不在，BBC 希望用 micro:bit 复制他们的成功。与 BBC Micro 不同，这不是一台配有键盘和显示器的普通电脑。相反，它是一个基于 ARM 芯片的微控制器开发平台。现在，[micro:bit 正在成为 Python](http://ntoll.org/article/story-micropython-on-microbit) ，这是当今的基础，并且肯定会在英国的课堂上更加有用。

Python 在 micro:bit 上的最初开发始于使用微软的 [TouchDevelop](https://github.com/Microsoft/TouchDevelop) 作为基于浏览器的 IDE，将 C++代码发送到 mBed 云编译服务。将生成一个十六进制文件，该文件将被下载到本地文件系统，最后学生只需将该十六进制文件拖到 micro:bit 上，因为它在桌面上显示为 USB 存储设备。这是一个可怕的想法，[因为 MicroPython 存在](https://micropython.org/)。当前在 micro:bit 上运行 Python 的方法非常简单，只需将其插入 USB 端口，打开一个终端，然后编写一些代码。这是你能接触到的最接近带有 BASIC in ROM 的计算机，也是数百万 11 岁儿童学习如何编码的最佳设备。

谢谢你的提示。