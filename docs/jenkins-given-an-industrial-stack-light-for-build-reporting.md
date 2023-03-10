# Jenkins 为构建报告提供了一个工业堆栈灯

> 原文：<https://hackaday.com/2017/09/05/jenkins-given-an-industrial-stack-light-for-build-reporting/>

当在团队环境中进行软件开发时，随时了解构建的状态是很重要的。Jenkins 可以在屏幕上显示构建自动化信息，但是这有什么意思呢？一个流行的 office 项目是构建某种项目状态的可视化显示，而[dkt01]已经用这个 [stack light build monitor](https://hackaday.io/project/26995-stack-light-monitor) 做到了这一点。

在今天这个网上购物的时代，随机的工业硬件只是一个易贝，所以很容易找到一些很酷的灯或任何项目的指标。[dkt01]从货架上购买了一个标准的 24V 堆栈灯。它有绿色、红色和黄色指示器，非常适合显示构建服务器的当前状态。

该项目使用 Arduino Pro Micro 结合 ENC28J60 以太网适配器。我们过去一直都可以看到这种芯片，但在 2017 年，它有点像一个经典的设置，大量未清洗的人群大量迁移到 ESP8266。然而，对于这个项目来说，它非常适合连接到有线办公室网络(毕竟，您想知道您的构建状态，而不是您的 WiFi)。[dkt01]尽管 ATmega32u4 的资源相对贫乏，但还是设法让网络配置工作起来。

构建过程非常干净，微控制器和以太网硬件被嵌入到堆栈灯外壳的 3D 打印底座中。如果它是一个整洁的建筑，没有到处悬挂的电线，那么定制的 PCB 将所有东西整齐地连接在一起，它更有可能成为永久的办公室设备。另一个巧妙之处是，堆栈灯在初始化时闪烁，指示 DHCP 租借是否成功，这使得故障排除更加容易。休息后，视频中有所有不同灯光组合和含义的概述。

总的来说，这是一个可靠的构建，使用了一些现成的组件，服务于一个真正的目的。对于一个较小规模的类似项目，[查看指标](http://hackaday.com/2011/04/12/led-build-monitor-helps-keep-an-eye-on-your-servers/)。更重要的是，向我们展示你是如何学会在城市的交通灯上输出你的服务器状态的。不过，先问一下。


 [https://www.youtube.com/embed/2Hm4lpO7gss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2Hm4lpO7gss?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

