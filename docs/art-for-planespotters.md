# 飞机观察者的艺术

> 原文：<https://hackaday.com/2015/12/31/art-for-planespotters/>

我们不懂艺术，但我们知道自己喜欢什么。约翰·坎弗洛的这个小发明正符合我们的胃口。

首先，[Johan]把一台旧的 Macintosh 经典电脑的内部掏空，[在里面塞了一个树莓派。现在这是](http://johan.kanflo.com/another-raspberry-pi-powered-macintosh-classic/)[不是一个真正的新想法](http://hackaday.com/2014/02/11/the-mac9000-a-photo-frame-with-style-maybe/)，但【约翰】在显示器上做得非常好，他对重建的软驱弹出机制细节的关注。他还给它特有的“沉闷”噪音。

然后，他给树莓派配备了一个运行 [dump1090](https://github.com/antirez/dump1090) 软件的 RTL 加密狗来监听 ADS-B 无线电信号。从 SDR [中提取的数据通过管道传输到 MQTT 服务器](https://github.com/kanflo/ADS-B-funhouse)，上面有关于头顶上飞机的各种数据。另一个脚本订阅 MQTT 主题，并计算出哪个是最接近的，然后对有问题的平面类型运行图像搜索，将结果发布回另一个 MQTT 主题。[最后一个脚本](https://github.com/kanflo/adsb-skygrazer)订阅了最后一个主题，并在屏幕上显示相关图像。Pshwew！

最终的结果是一个麦金塔经典，它会随着最接近头顶的平面不断更新。我们根本不确定这是否是美术，或者是有用艺术的一部分，或者可能以上都不是。但是我们真的很喜欢这个不错的 case 工作，并且认为使用 MQTT 作为后端来协调多个并发 Python 脚本(在同一台计算机上)非常酷。