# 用 OpenCV 对数控铣床进行零位调整

> 原文：<https://hackaday.com/2016/12/15/zeroing-cnc-mills-with-opencv/>

对于[Jay]和[Ricardo]在康奈尔大学[Dr. Bruce Land]的 ECE4760 课程的最终项目，他们解决了一个困扰所有机械师的问题。他们的项目使用计算机视觉在数控机床[中找到一个零件的 XY 零点，大大减少了设置工件所需的时间，并给了我们另一个理由来淡化“物联网”这个词，称之为数控机床的互联网。](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2016/jdf258_rls454/jdf258_rls454/jdf258_rls454/index.html)

对于硬件，[Jay]和[Ricardo]使用 PIC32 与一个 [Arducam 模块](http://www.arducam.com/)、一个 WiFi 模块和一个感应传感器连接，用于测量到工件的距离。所有这些都集成在一个专门设计为单面的 PCB 上(智能！)，并藏在一个可以轻松连接到数控铣床主轴的外壳中。这个奇妙的装置俯视一个工件，并使用 OpenCV 找到夹具上的一个孔的中心。找到中心后，铣削在其 XY 轴上归零。

该软件比在微控制器上运行 OpenCV 处理的设备简单一些。例如，检测孔的中心发生在运行一些 Python 脚本的笔记本电脑上。mill attachment 通过 WiFi 与笔记本电脑进行通信，并将向下摄像头的一些图像发送到笔记本电脑。从那里，笔记本电脑检测夹具板中孔的中心，并生成一些 g 代码发送到工厂。

虽然该设备工作非常好，并且能够相当快速地对中研磨机，并且不需要大量的用户干预，但是仍然存在一些问题。相机没有完全对准主轴的轴线，这使得数学计算比它应该的更难。此外，这种外壳并不是一个冷却液到处喷洒的环境。这些都是小问题，这些问题可以简单地通过设计和打印另一个附件来解决。不过，这种设备确实有效，而且真的减少了清除一个工厂所需的时间。

你可以看看下面的视频描述。

 [https://www.youtube.com/embed/MGF50TGyLYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MGF50TGyLYQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

