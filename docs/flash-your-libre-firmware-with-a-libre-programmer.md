# 用 Libre 编程器刷新你的 Libre 固件

> 原文：<https://hackaday.com/2018/05/26/flash-your-libre-firmware-with-a-libre-programmer/>

无论你个人是否同意自由软件基金会(FSF)的所有理念，你都必须给予他们信任:他们不会乱来。他们开始为一个免费的开源操作系统打下基础，然后一旦这个梦想实现，就开始推动用 Libreboot 这样的开放替代软件取代专有 BIOS 固件的想法。但是很明显，即使这样也不够，因为还有更多的自由等待着我们。各位，我们现在在玩 4D 自由象棋。

[![](img/7e8f0151f75728abd08d080b689286d7.png)](https://hackaday.com/wp-content/uploads/2018/05/zerocat_detail.jpg) 要在运行 libre 操作系统的电脑上刷新 libre 引导固件，而不涉及任何专有的有趣业务，你需要一个 libre 芯片程序员。幸运的是，[FSF 刚刚授予 Zerocat Chipflasher“尊重你的自由”认证](https://www.fsf.org/news/zerocat-chipflasher-board-edition-1-now-fsf-certified-to-respect-your-freedom)，这意味着该产品的每个元素都是在免费许可下发布的，供你享受黑客乐趣。据 FSF 称，这是他们向用户提供一台真正免费的开源计算机的目标的一个重要里程碑，从浏览器一直到 BIOS。

当然，你不需要成为理查德·斯托尔曼来欣赏一个完全开放的芯片程序员。借助 Chipflasher 网站上提供的软件、接线图和 PCB 文件，该项目是一个极好的教育参考。这也意味着，有了 Chipflasher 的 Git 库的克隆，你就可以很好地构建你自己的设备了。

鉴于第一代 Zerocat Chipflasher 的价格标签大约为 350 美元，我们很可能会在不久的将来看到这款设备的一些 DIY 版本。这并不是说我们想剥夺 Zerocat 在这个非常简洁的设备上的商业成功，但对许多人来说，这是一个非常昂贵的价格；即使你获得了所有的自由。

它可能会使用一种比 Zerocat Chipflasher 稍微模糊一点的设备，但如果你想了解 BIOS 更换的高风险世界，我们自己的[【Bryan cock field】记录了在 Thinkpad X200](https://hackaday.com/2016/12/16/installing-libreboot/) 上安装 Libreboot 的传奇故事。不惜一切代价[让英特尔管理引擎离开](https://hackaday.com/2017/12/11/what-you-need-to-know-about-the-intel-management-engine/)你的企鹅动力机器。