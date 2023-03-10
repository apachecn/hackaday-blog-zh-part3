# Jenkins 和 Slack 报告构建失败！点燃烽火！

> 原文：<https://hackaday.com/2016/11/19/jenkins-and-slack-report-build-failure-light-the-beacons/>

当您有一个大型软件开发团队在一个项目上工作时，监控构建服务器是该过程的一个重要部分。当来自构建服务器的消息到来时，你需要从你正在做的事情中抽出时间来确保构建没有被破坏，如果它是因为你所做的事情而被破坏的，你必须停止你正在做的事情，开始修复它，并让人们知道你正在处理它。

[ridingintraffic]的团队使用 Jenkins 来自动构建他们的项目，如果有问题，它会向 Slack 频道发送消息。这意味着团队需要监控松弛通道，这会导致一些延迟。[ridingintraffic]想要立即了解构建问题，因此[借助一些软件、物联网硬件和旋转危险警示灯](https://hackaday.io/project/18006-jenkins-build-pipeline-failure-notification)，团队现在可以看到一条可见消息，表明存在构建问题。

Adafruit Huzzah ESP8266 板用作控制器，通过 434MHz 无线电模块连接到一些 RF 控制的电源插座。为了制作该系统的原型，[ridingintraffic]使用了一个连接到其中一个射频模块的 Arduino 来嗅出遥控开关电源插座的代码。有了代码，Huzzah 板的工作就开始了。

MQTT 代理用于让 Huzzah 知道构建失败的时间。如果有，Huzzah 通过电源插座打开灯标。运行在 Slack 通道上的 bot 侦听来自一个开发人员的消息，该消息表示问题正在解决中，当它得到消息时，它向 MQTT 代理发送一条消息，关闭信标。

内部网络、Huzzahs 和互联网上的 Slack 服务器之间也有一些分离，[ridingtraffic]在一篇更详细的[博客文章](https://tech.cars.com/the-beacons-are-lit-jenkins-calls-for-aid-7fcfc1af14ea#.afg3zv6jl)中回顾了用于各层之间通信的方法。现在，[ridingtraffic]办公室里的开发人员不需要粘在 Slack 频道上，当它发出开始恐慌的信号时，他们不会错过信标！