# 詹金斯点亮了圣诞树

> 原文：<https://hackaday.com/2016/12/27/jenkins-lights-the-christmas-tree/>

Jenkins 是一款开源自动化软件，它试图将软件开发过程的一部分自动化。例如，当你提交代码时，Jenkins 会获取它，用它构建项目，并在其上运行任何测试。如果有大量的人提交新的代码或数据，Jenkins 会等待并抓取一堆提交来构建。根据项目的大小，这可能需要一段时间，如果有问题，您需要尽快知道，这样人们就不会等待一个不完整的构建。电子邮件对此没有问题，但[dkt01]在 Hackaday 上看到了一个桌面 LED 圣诞树项目，并将其集成到他的 Jenkins 系统中。

像其他项目一样，WS2812b LED 环被用作树，Arduino Pro Mini 运行该节目，带有一个以太网 LAN 模块，与监控 Jenkins 构建作业的 Python 脚本进行通信。Python 脚本向 Arduino 发送命令，Arduino 依次点亮 led。如果构建成功，它们会亮起绿色，如果失败，则会亮起红色，但在构建过程中，led 会显示构建的当前状态，在构建过程中跟踪 Jenkins 的进度。 

我们之前的 [Jenkins post](https://hackaday.com/2016/11/19/jenkins-and-slack-report-build-failure-light-the-beacons/) 使用了一个巨大的红色 LED 灯，如果构建失败，它就会亮起。[dkt01]的构建让您知道构建是成功还是失败，但是构建进度是一个很好的补充。

 [https://www.youtube.com/embed/l4QfoKM_p1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/l4QfoKM_p1U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

