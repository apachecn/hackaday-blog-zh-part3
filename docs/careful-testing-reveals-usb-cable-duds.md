# 仔细测试揭示 USB 电缆哑弹

> 原文：<https://hackaday.com/2018/02/02/careful-testing-reveals-usb-cable-duds/>

有什么比第一次启动你的最新版本却什么都没发生更糟糕的呢？好吧，也许这不像释放魔法烟雾那么糟糕，但没有一盏闪烁的灯像预期的那样闪烁，这仍然很令人困惑。

此时你所做的很大程度上取决于你的故障排除方式，当[Scott M. Baker]的 Raspberry Pi jukebox 构建失败时，他回到基本原则，检查了电源线。这被证明是罪魁祸首，但他没有就此放弃，而是对多条 USB 电缆进行了一系列彻底的负载测试，以查看哪些电缆是可疑的，并获得了有趣的结果。

[Scott]最初使用一端带 USB-A、另一端带 3.5 毫米筒形插头、中间带开关的电缆，假设 Pi 端的插头会更结实，并为自动点唱机配备电源开关。使用可调 DC 负载测试该电缆将证明该电缆不适合 Pi 负载，在区区 500mA 负载下电压降至 2 伏以下。事实证明，其他电缆在负载下要好得多，甚至是那些带有 USB 迷你插孔的电缆，甚至是一个带有 5.5 毫米圆筒的电缆。但是更大的桶形插头电缆在与内嵌开关配对时也很讨厌。在下面的视频中，[Scott]不仅介绍了测试过程，还简要介绍了他自制的 DC 负载。

教训很明显:不是所有的 USB 电缆都是一样的，所以警告黑客。如果你也像[Scott]一样渴望检查垃圾箱里的电缆，[这款全功能智能 DC 装载机](https://hackaday.com/2017/11/12/smart-dc-tester-better-than-a-dummy-load/)可能正是你想要的。

 [https://www.youtube.com/embed/odu17lhN-vk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/odu17lhN-vk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[via [危险原型](http://dangerousprototypes.com/blog/2018/01/31/measuring-usb-power-cable-voltage-drop-with-my-dc-load/)