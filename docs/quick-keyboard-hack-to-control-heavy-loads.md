# 快速键盘黑客控制重负荷

> 原文：<https://hackaday.com/2015/09/18/quick-keyboard-hack-to-control-heavy-loads/>

当你想从电脑上控制一个外部设备(比如灯)时，你可以使用一个支持 USB 的微处理器。寻找一个便宜快捷的选择来控制两个灯【Pete】想要控制两个 12 伏的卤素灯，[他伸手去拿键盘，用了一点 python](http://junkstation.weebly.com/usb-keyboard-switched-drives.html) 。

台式电脑键盘有 3 个 LED 指示锁定功能，几乎没有人使用滚动锁，在没有键盘的笔记本电脑上，numlock 也没有什么大的损失。将电线添加到 USB 键盘外的小 PCB 上 numlock 和 scroll lock LED 的 5 伏输出被重定向到开关电路。

该开关电路接收任一 LED 的输出，用 PNP 晶体管将其反相，然后连接到 FQP30N06L“逻辑电平”mosfet 晶体管的栅极，以处理繁重的负载。一旦接线到位，一个相当简单的 Python 脚本就可以接管打开和关闭两个选定的锁键，只需按一下按钮就可以控制高达 32 安培的电流。