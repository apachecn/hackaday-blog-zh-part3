# 圣诞之星使用两节 AA 电池

> 原文：<https://hackaday.com/2015/12/16/christmas-star-uses-two-aa-batteries/>

当[hkdcsf]还是一个少年时，他制作了一个圣诞星，用一个上行计数器驱动解码器逻辑，并用晶体管点亮节日图案的 led。[他使用现代技术重新审视了这个项目](https://hackaday.io/project/8685-xmastar)，包括微控制器、DC/DC 转换器和恒流 LED 驱动器。

该项目使用两节 AA 电池，这就是为什么 DC/DC 转换器是必要的。蓝色 LED 的正向电压刚刚超过 3V，LED 驱动芯片需要大约 0.6V 的开销。两个新的 AAs 将运行略高于 3V，但当它们放电时，或者如果他使用可充电电池，就不会有足够的潜力。为了确保 star 即使在选择任何 led 的情况下也能工作，转换器从电池中取出标称的 3V，并将其转换为 3.71V。

微控制器可以依靠 DC/DC 转换器的电压或者直接依靠电池工作。该转换器非常重要，因为控制器会在睡眠模式下禁用 DC/DC 转换器，以节省电池寿命。PIC16LF1703 将运行到 1.8V，功耗非常低，尤其是在睡眠模式下。

LED 驱动器从 PIC 接收 SPI 命令，并打开 LED。PIC 上的软件使用状态机架构来驱动您在下面的视频中看到的动画。

项目文档令人印象深刻，包括软件和硬件的高级概述。还有范围捕获和驱动[hkdcsf]设计决策的信息。星形 PCB 的触感也很好。

当然，我们已经看到[树莓树](http://hackaday.com/2014/11/09/deck-the-halls-with-a-raspberry-pi-controlled-christmas-tree/)，圣诞树[变成了二进制时钟](http://hackaday.com/2014/12/10/the-epoch-christmas-tree/)。不过，我们想知道[hkdcsf]是否计划在 LED 烛台上使用相同的硬件和软件[。](http://hackaday.com/2008/11/09/led-menorahs/)

 [https://www.youtube.com/embed/3nNxpWl-rJ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3nNxpWl-rJ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

