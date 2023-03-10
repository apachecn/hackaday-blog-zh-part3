# 用于自启动开关的螺线管和伺服系统

> 原文：<https://hackaday.com/2018/01/18/solenoids-and-servos-for-self-actuated-switches/>

家庭自动化的新热点是 WiFi 控制的电灯开关。当然，我们用 X10 模块实现计算机控制的家庭照明已经有 40 年了，但现在我们有风险投资资金涌入硬件，有人需要赚钱。几年前，[Alex]在他家的一些设备中安装了 WiFi 开关，并发现了电灯开关互联网的一个缺点——他的电灯开关没有令人满意的手动控制。亚历克斯没有因为缺少联网蜡烛而诅咒黑暗，而是做了唯一明智的事情。他在家里的电灯开关后面安装了电磁铁、螺线管和伺服系统。

[Alex]在这里试图解决的确切问题是有状态墙壁开关。有了连接互联网的灯插座，墙壁开关不再工作。当你的手机没电的时候能够开灯是我们都认为理所当然的事情，当然，解决方案是拥有联网开关。

能够读取交换机的状态并向服务器发送一些数据是很容易的。为此，[Alex]使用了一个简单的基于 ESP8266 的板。不过，这里的诀窍是状态开关可以自己开关。这是一个机械建筑，虽然存在可以通过计算机命令上下翻转的自动开关，但它们非常昂贵。相反，[Alex]走了 DIY 路线，首先在开关后面安装电磁铁，然后转向螺线管，最后围绕四个廉价的业余爱好伺服系统设计了一个解决方案。整个虚构被塞进一个 2 宽的电气盒，由两个开关、四个业余伺服系统、D1 迷你和一个[阿达果伺服驱动板](https://www.adafruit.com/product/815)组成。

整个设置的软件栈包括一个 NodeJS 服务器，它通过 UDP 连接到 Orvibo 智能套接字。该服务器上还有一个 WebSocket 服务器，用于基于浏览器的客户端打开和关闭灯光，一个 FauXMo 服务器，用于通过 WeMo 仿真通过 Amazon Echo 打开和关闭灯光，还有一个 HTTP 服务器，用于其他客户端，如[Alex]的 Pebble Watch。

毫无疑问，这是我们见过的最巴洛克式的开灯和关灯方法。尽管有这种惊人的复杂性，但[Alex]有一些使用起来也很直观的东西，借用一句应用主义的话，“就是管用”。有了这样的设置，任何人都可以通过互联网轻按开关，打开或关闭灯，反之亦然。这是我们见过的最好的家庭自动化产品。

你可以在下面查看[Alex]的视频演示，或者在这里查看整个项目的 GitHub。

 [https://www.youtube.com/embed/lpp6qdrYlEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lpp6qdrYlEQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

