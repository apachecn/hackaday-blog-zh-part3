# 猎鸭——阻止橡皮鸭的攻击

> 原文：<https://hackaday.com/2016/10/28/duckhunting-stopping-rubber-ducky-attacks/>

一天早上，一个戴着巴拉克拉法帽的黑客走进你的办公室。你认为是同事，因为他戴着头套。黑客将一个 u 盘插入隔壁房间的一台电脑。奇怪的命令行工具出现在屏幕上。几分钟后，你的整个公司都暴露了。这个流氓手里拿着一个拇指驱动器快速的撤退了。

这是巴拉克拉法帽和 USB 橡皮鸭供应商想象的场景，微型 USB 设备能够注入代码，运行程序，并从任何系统提取数据。防止这种攻击的最佳方式——也是最常见的方式——是用环氧树脂填充 USB 端口。[pmsosa]认为应该有一种软件方法来防御这些橡胶鸭子，所以[他创建了 Duckhunter，](https://github.com/pmsosa/duckhunt)一个小型、高效的守护程序，可以捕捉并阻止这些漏洞。

橡皮鸭攻击只是打开一个命令行，从一个模拟的 USB HID 键盘发起攻击。如果攻击者不能打开 cmd 或 PowerShell，攻击就中断了。这对于编码来说很简单，但是[pmsosa]还有一些锦囊妙计。Duckhunter 有一个“偷偷摸摸”的对抗功能，每 5-7 次击键中就有一次被阻止。对攻击者来说,“偷偷摸摸”的对策让攻击看起来好像成功了，但实际上它失败了。

有许多不同的攻击类似于橡皮鸭所能完成的。Mousejack 通过蓝牙进行同样的攻击。 [BadUSB](http://hackaday.com/2014/10/05/badusb-means-were-all-screwed/) 更具技术性，它允许任何能够访问设备固件的人用你自己的键盘攻击你。由于攻击的性质，Duckhunter 将它们全部关闭。

目前这个版本只针对 Windows，但是根据[【PMS OSA】的 GitHub](https://github.com/pmsosa/duckhunt) 消息，将会有 Linux 和 OS X 版本。