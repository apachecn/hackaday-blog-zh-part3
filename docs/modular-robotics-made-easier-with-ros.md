# ROS 让模块化机器人变得更简单

> 原文：<https://hackaday.com/2018/05/31/modular-robotics-made-easier-with-ros/>

机器人由许多硬件组成，每个硬件都需要自己的软件。即使是一个带有少量伺服电机的小型机械臂也使用伺服电机库。

给轮式车辆加上这个手臂，你就有了更多的马达。然后附加一些超声波传感器用于防撞或者一个摄像头用于视觉。到那时，你可能已经把软件分成了多个进程:一个用于手臂，另一个用于移动，一个用于视觉，还有一个作为大脑以某种方式与所有其他部分接口。视觉[可能在做物体识别](https://hackaday.com/2017/06/06/self-driving-rc-cars-with-tensorflow-raspberry-pi-or-macbook-onboard/)，这是一件计算量很大的事情，所以你现在有多台计算机。

将所有这些复杂性分解成模块，你就有了机器人操作系统 ROS 的用例。正如本文所示，ROS 可以帮助设计、构建、管理甚至进化您的机器人。

## ROS 是什么？

ROS 是一个由大量专门用于开发机器人的库和工具组成的框架。它是开源的，大部分代码都在 BSD 许可下。它也是社区支持的。

ROS 主要在 Ubuntu 和 Mac OS X 上测试，尽管社区也让它在其他 Linux 发行版和 Windows 上运行。我在我的树莓派 3B 上运行了 [Ubuntu 16.04 下的 ROS 动态释放。](https://downloads.ubiquityrobotics.com/pi.html)

[![Robot arm simulation in Gazebo](img/299855a6d355292e7388bd828e00fe10.png)](https://hackaday.com/wp-content/uploads/2018/05/ros-gazebo-robot-arm-simulation3.jpg)

Robot arm simulation in Gazebo. Photo from [The Construct](https://www.youtube.com/watch?v=DJwnZSaHy7s)

## 模拟你的机器人

在你建造你的机器人之前，你可能希望先模拟它。为此，您可以创建一个统一机器人描述格式(URDF)文件，这是一个详细描述您的机器人的 XML 文件。甚至还有一个适用于 SolidWorks 的 URDF 出口商插件。然后，在建造任何东西之前，你可以将它与 ROS 和 Gazebo 机器人模拟器一起使用，在屏幕上查看和操纵你的机器人。

## 在 ROS 中构建事物:包

很难解释 ROS 有哪些功能，而不回顾一下这些功能是如何构建的。

在层次结构的顶部，您的机器人应用程序由一个或多个包组成。包通常包含代码、库、数据集和配置文件。任何可以作为一个模块放在一起的东西都应该放在一个包里。也许你已经将 Arduino Nano 专用于伺服电机控制器。你可以把所有与 Arduino 通信的文件放到他们自己的包里。

运行 ROS 命令，命令行中的`rospack list`列出了 229 个包。这里有一个小例子。

raspicam_node 包是我在网上找到的[包，眼球包是我从头开始创建的。](https://discourse.ros.org/t/raspberry-pi-camera-node/1388)

软件包是由一个大型社区贡献的。例如，业余爱好者有流行的 Pololu 电机控制器包，工业界有 KUKA 和 Baxter 机器人包。这里是[一个可用软件包](http://rosindex.github.io/packages/page/1/time/)的大列表的链接。网上搜索找到更多。

## 流程是节点

![Nodes in ROS](img/ca3306944734583401b8740660bb9caa.png)

一个足够复杂的机器人将需要多个过程，甚至可能分散在不同的计算机上。在 ROS 中，每个进程都是一个节点。一个包包含一个或多个节点。

对于我的例子，我使用 raspicam_node，它从 Pi 摄像机读取并产生一个压缩的视频流。一个名为 image_republisher 的节点解压缩该视频。然后我的眼球节点处理视频中的图像。当然，要做到这一点，他们需要以某种方式交流。

## 节点之间的通信

ROS 为节点相互通信提供了两种机制。

一种是发布-订阅机制，其中一个节点发布它将有数据可用。它以一个名为主题的名字出版。在此处所示的示例中，raspicam_node 将压缩视频发布到主题/raspicam _ node/image/compressed。需要该数据的节点，在我们的例子中是 image_republisher，然后订阅该主题。当发布者准备好压缩的视频图像时，发布者发布它，订户将接收它。

另一种通信机制称为服务。服务器节点提供服务，客户端节点请求该服务。与发布-订阅一样，服务器通过主题名来公开其服务，而客户机通过该主题来找到服务。与发布-订阅不同，是客户端节点发起通信。每当它需要服务时，它就这样做。

注意，对于这两种机制，通信都是使用主题发起的，而不是通过直接寻址任何特定的节点。如果你测试不同的电机控制器，你可以写不同的节点，它们都使用相同的主题。一次测试一个，订阅者将会找到恰好运行的那个，因为它使用主题而不是任何特定的电机控制器来进行查找。如果您决定以后更换硬件，或者在硬件需要维护时使用存根，这也很有用。

ROS 还在通信节点之间提供了某种语言独立性。ROS 支持 Python 和 C++。发布者可以用 Python 写，订阅者可以用 C++写，反之亦然。例如，只要有数据可用，Python 发布者就可以收集传感器数据，而 C++订阅者则负责繁重的处理工作。

主题是如何映射到特定节点的？主进程会处理这些。

## 分布式计算

![Momaro](img/1f6d036d7a73ff49e78558bd9b6606d1.png)

Momaro, Photo [frontiers in Robotics and AI](https://www.frontiersin.org/articles/10.3389/frobt.2016.00057/full)

节点可以通过机器网络相互通信。主服务器只在一台机器上运行。所有其他机器上的节点使用包含拥有主节点的机器的主机名的环境变量来查找主节点。

当节点请求发布或订阅主题时，它们只给出主题名称。某一天发布节点可能在一台机器上，而第二天它可能在另一台机器上。订户不会知道这一点。他们只需订阅主题名，然后由站长负责寻找发布者。

例如，想象一个半人马机器人，它的躯干可以连接到不同的移动平台上。一旦物理连接，躯干中的节点必须找到移动平台中的节点。如果所有平台都使用相同的主题名称，那么无论使用哪个平台，都会找到节点。这里展示的机器人 Momaro 只是为了说明，因为它有一个只有一个 CPU 的永久底座。但是，它确实使用了 ROS。

## 可视化工具

有一些有用的命令行和图形工具可以帮助管理和调试包、节点、主题和通信。一些命令行工具是 rospack for packages、rosnode 和 rostopic。

[![rqt_graph showing nodes, topics and how they're communicating](img/5d6830f209caac3d932b83f93afb9816.png)](https://hackaday.com/wp-content/uploads/2018/05/rqt_graph_output.png)

rqt_graph showing nodes, topics and how they’re communicating

Rqt_graph 以图形方式显示节点、主题以及节点之间的通信方式。在这里，我们再次看到/raspicam_node/image/compressed 是订阅来自 raspicam _ node 的压缩视频图像的主题，而/raspicam_node/image 是订阅未压缩图像的主题。该显示可能会突出显示通信问题。

![rqt_console and rqt_logger_level showing possible issues with raspicom_node](img/55b587b1f08084e2621d1de2ff31e3da.png)

rqt_console and rqt_logger_level showing possible issues with raspicom_node

rqt_console 和 rqt_logger_level 一起显示从节点记录的消息，无论是严格的信息性消息、警告还是错误。它们对于调试和故障排除非常有用。

## 欢迎模块化机器人

这是 ROS 可以帮助你实现机器人模块化的一个很大的例子，从设计和仿真到调试和故障排除。

你有使用 ROS 的机器人吗？也许你会想让它参加 2018 年[黑客奖](https://hackaday.io/prize)的[机器人模块挑战赛](https://hackaday.io/prize/details#two)，但请抓紧时间。6 月 4 日的最后期限很快就要到了。即使你不参加比赛，我们仍然想听听你和 ROS 的经历。请在下面的评论中告诉我们。

同时，我们将为您留下一段视频剪辑，展示使用 ROS 的机器人。

[https://player.vimeo.com/video/146183080](https://player.vimeo.com/video/146183080)