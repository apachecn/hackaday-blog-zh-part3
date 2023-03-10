# 用 Raspi 夜视摄像机对光线的消逝表示愤怒

> 原文：<https://hackaday.com/2017/11/29/rage-against-the-dying-of-the-light-with-a-raspi-night-vision-camera/>

关于黑客最有趣的事情之一是我们在开始时的愿景和我们在结束时建立的现实之间的差异。[对于【无面者】来说，开始时只是一个简单的计划，要制造一个夜视虚拟现实耳机，结果却变成了一场长达五个月的冒险，最终完成了这个漂亮的相机](https://hackaday.io/project/27544-night-vision-camera-raspberry-pi)。他认为这很容易，但几乎每个方面都存在某种挑战。重要的是他坚持下去了。

[无面者]遇到的主要问题之一是权力。他发现 Pi(零 W)、屏幕和红外 led 总共消耗 1.5 到 2A 之间的能量。他通过使用 2A 电力银行的充电板和一台 1200mAh 的 Li-Po 解决了这个问题，该 Li-Po 是为 vaping 所需的高功率而制造的。如果不是因为空间问题，他可能会使用 18650 或两个。

他面临的另一个挑战是存储视频和图像。他曾考虑将 Pi 设置为从手机浏览器查看它们的接入点，但最终用 OTG 电缆扩展了 USB 端口，以使用闪存驱动器。使用一点 Python，他可以观察要安装的驱动器，然后向其写入。如果闪存盘突然消失，Pi 开始保存到 SD 卡。

休息之后有两个视频，一个是演练，一个是夜视演示。你会在演示视频中看到一点延迟——这是因为[无脸失败者]首先通过 PyGame 运行 feed。无论你想窥视什么样的夜生活，用测距仪添加自动变焦功能或者用望远镜近距离观察 T2 都是不错的选择。

 [https://www.youtube.com/embed/2aCs_iUty_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2aCs_iUty_g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/BGtsTNCMrQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BGtsTNCMrQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

