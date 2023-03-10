# ZeroPhone 让智能手机相形见绌

> 原文：<https://hackaday.com/2017/01/18/zerophone-gives-smartphones-the-raspberry-pi/>

现在有几款开源手机，但是它们都有缺点。难以获得零件、难以焊接或难以编程的系统比比皆是。[Arsenijs]希望通过零手机改变这一切。ZeroPhone 基于流行的 Raspberry Pi Zero。CPU 模块 5 美元的价格标签意味着你可以花大约 50 美元来制造整个手机。

ZeroPhone 中的无线电模块是众所周知的 SIM800L 2G 模块。在许多地方，2G 正在消失，所以[Arsenijs]已经在研究更现代的设备。一个 ESP8266 作为 WiFi 模块，带有有机发光二极管屏幕和 python 代码来完善这款手机。当然，它不是一个花哨的图形触摸屏，但完整的桌面只是连接显示器、鼠标和键盘的问题。

对于安全意识，零电话提供了一个独特的控制水平。因为这是一个运行 Linux 的 Raspberry Pi，所以您可以选择哪些模块包含在内核中，哪些软件加载在文件系统中。有消息称[我们可能很快就会有一个 blobless Pi](http://hackaday.com/2017/01/14/blob-less-raspberry-pi-linux-is-a-step-closer/) ，藏在无线电模块中的固件是仅存的黑匣子。

如果树莓派对你来说有点难以下咽，看看这款基于 Arduino 的手机。不想做什么锡焊？看看你能用一部[廉价安卓手机和一点黑客技术](http://hackaday.com/2015/09/10/want-a-low-cost-arm-platform-grab-a-prepaid-android-phone/)做些什么。