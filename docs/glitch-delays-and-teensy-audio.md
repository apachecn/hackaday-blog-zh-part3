# 毛刺延迟和微弱音频

> 原文：<https://hackaday.com/2018/01/11/glitch-delays-and-teensy-audio/>

随着 Teensy 3.6 和相关音频处理库的发布，现在是开始 DIY synth 和 effects 项目的最佳时机。[斯科特]是一名音乐家和电子乐器制造商，所以他决定利用青少年的力量，制作一个延迟模块，这真的没有其他方法可以做到。

这种延迟模块的功能有点类似于多头基于磁带的延迟，只是在数字域之外是完全不可能的。在一个循环缓冲器上有四个“读取头”。前三个头以不同的速度在缓冲区内播放小循环，一个以原始速度播放，一个以半速播放(低一个八度)，一个以双倍速度播放(高一个八度)。第四个头不循环，反而反过来播放延迟缓冲。当然，有方便的旋钮来设置每个“读取头”的水平。

这个项目是围绕[【Scott】的 JUCE 框架](https://github.com/cutlasses/TeensyJuce)的移植构建的，这是一个非常强大的音频 API，现在非常适合笔记本电脑和嵌入式开发。这个项目的文件都可以在 GitHub 上获得，[Scott]计划为所有参数的 CV 控制建立一个扩展模块。

那么，这种故障延迟听起来如何？非常好。下面的视频只是一个到一个活套踏板的 tele，和到毛刺延迟。肯定有一些后摇滚明星在这件衣服上弄湿了他们的紧身牛仔裤，这是对青少年音频处理能力的一个很好的应用。

 [https://www.youtube.com/embed/sdTysy3dD84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sdTysy3dD84?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

