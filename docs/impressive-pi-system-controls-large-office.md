# 令人印象深刻的 Pi 系统控制大型办公室

> 原文：<https://hackaday.com/2016/10/22/impressive-pi-system-controls-large-office/>

当构建一个系统来控制一个大办公室时，大多数人不会想到一堆覆盆子馅饼，但大多数人不是这样。当他们搬到一个更大的空间时，他决定使用 Pis 来管理他的公司 Monterail 的办公室。他们建造的系统是我们见过的最大的 Pi 装置之一，控制灯光、电视、扬声器和门禁。这一切都可以通过网络界面来控制，因此网络上的任何人都可以开灯或关灯，检查房间是否有人，或者将声音和视频发送到会议室的高级 AV 系统。他甚至黑掉了一堆 HDMI 开关，这样如果每个人都想看同一场比赛，每台电视都可以显示相同的图像。就连休息室里播放的广播电台也是通过员工空闲频道远程控制的。

该系统在五个 pi 上运行，其中一个充当主机，而其他的连接到每个电视，通过 [Chrome 调试协议](https://developer.chrome.com/devtools/docs/debugger-protocol)远程控制控制台模式下运行 Chrome。这使得网络上的任何人都可以控制显示器并向其发送内容。值得注意的一件有趣的事情是:[Kamil]坦率地承认这是一个定制的系统，不容易作为产品出售。这没有错，但他决定建立一些备份:如果整个系统发生故障，所有的灯，门和其他设备仍然可以通过老式的开关，钥匙和遥控器来控制。即使整个系统崩溃也不会导致办公室无法使用。这是一个广泛的预防措施，许多人在这样的系统中忘记了。