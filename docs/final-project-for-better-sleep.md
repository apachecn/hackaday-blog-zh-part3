# 改善睡眠的最终项目

> 原文：<https://hackaday.com/2017/12/17/final-project-for-better-sleep/>

又到了一年中的这个时候，世界各地的学生都在争先恐后地(或者已经争先恐后地)完成他们这学期的期末项目。虽然为期末考试而学习使许多人睡眠不足，但[Julia]和[Nick]正在寻求最大限度地增加[电气和计算机工程]专业允许他们的“少量睡眠”,方法是[用他们的期末项目来衡量睡眠质量](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/nas256_jbc262/nas256_jbc262/website/index.html)。

为了制定睡眠质量的衡量标准，[Julia]和[Nick]开始测量各种与睡眠相关的活动，特别是心率、运动和呼吸频率。在夜间，安装在手套上的 Arduino Nano 从安装在用户身上的各种传感器收集数据，同时将数据传送到固定的 PIC 进行分析和存储。当用户醒来时，他们可以在 PIC 基站的 TFT 显示屏上查看他们的睡眠报告。理想情况下，用户可以利用这些数据来测试不同的习惯，以获得最佳的夜间睡眠。

有趣的是，该小组选择实现他们自己的心率传感器。通过红外发射器、红外光电晶体管和运算放大器，该小组照亮用户的手指并测量反射以检测心跳。这是因为从用户手指反射的红外线量会随着血压和血氧水平的变化而变化，而血压和血氧水平在心脏跳动时也会发生变化。在谈到心跳传感器时，路上有些颠簸(需要使用手指而不是手腕迫使他们使用手套而不是腕带)，但我们认为它超级酷，完全值得。除了心率之外，加速度计还可以测量运动，缠绕在用户胸部的柔性传感器可以测量呼吸。

通过一对 nRF24L01s 传回的所有数据，PIC 计算出睡眠“混乱”，这正是它听起来的样子:它通过寻找非循环和突然的运动来描述用户睡眠有多混乱。使用这一指标，结合呼吸和心率的信息，PIC 计算出良好睡眠的百分比，其中 100%是一个美好的夜晚，0%意味着你可能已经度过了一个通宵。最重要的是，PIC 会将您的数据保存到 SD 卡中，便于事后查看。

为项目提供动力的注释代码可以在[这里](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/nas256_jbc262/nas256_jbc262/website/code/main.c)以及他们[项目报告](http://people.ece.cornell.edu/land/courses/ece4760/FinalProjects/f2017/nas256_jbc262/nas256_jbc262/website/index.html)中的部件列表中找到。

这款设备假设睡眠是问题所在，但如果醒来是你的问题，我们已经为你准备好了，[主动闹钟风格](https://hackaday.com/2017/08/03/the-alarm-clock-ate-my-duvet-cover-thats-why-im-late/)。对于那些已经进入睡眠状态的人，你可能需要[一些清醒梦的帮助](https://hackaday.com/2013/08/08/controlling-real-world-objects-from-your-lucid-dream-for-15/)。

休息后，由[Julia]和[Nick]讲解的项目视频。

 [https://www.youtube.com/embed/BiniQ5ze220?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BiniQ5ze220?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[Nick]发送此邮件！