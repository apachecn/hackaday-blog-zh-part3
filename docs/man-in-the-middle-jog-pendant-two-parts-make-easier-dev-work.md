# 中间人慢跑挂件:两个部分使开发工作更容易

> 原文：<https://hackaday.com/2018/01/11/man-in-the-middle-jog-pendant-two-parts-make-easier-dev-work/>

在一个项目中，打破开发工作流程的重复性任务令人难以置信地厌倦，甚至简单的自动化也能带来巨大的变化。[Simon Merrett]在一个应变波齿轮项目中测试不同的步进电机时遇到了这种情况。驱动电机的系统接受 g 代码，但他受够了仅仅让步进机按需旋转一点所需的开销。他的解决方案？一个由旋转编码器和 Arduino Nano 组成的 [grbl 中间人慢跑手控盒](https://hackaday.io/project/29627-grbl-man-in-the-middle-cnc-jog-pendant)。该单元忠实地传递从主机控制器接收的任何命令，但如果旋转编码器旋钮，它会发送定制的 g 代码，允许[西蒙]按需拨入一点加速度控制的电机旋转。下面是一个简短的演示视频，它让我们知道，当一些简单的电机运动只是旋转一个旋钮时，关注硬件的螺母和螺栓端是多么容易。

 [https://www.youtube.com/embed/9s8bzkdnVMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9s8bzkdnVMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[Simon]的 jog 挂件移动一个电机，这正是他使用同步带简化他的[3D 打印应变波齿轮的开发所需要的，但它可以用任何 g 代码编程。说到数控机床的 DIY 点动挂件，不要忘记](https://hackaday.com/2017/01/17/3d-printed-strain-wave-gear-needs-your-help/)[这个无线的是由 Atari 2600 操纵杆](https://hackaday.com/2015/01/24/atari-2600-controller-now-controls-cnc-plasma-cutter/)制成的，它在 X 和 Y 方向点动等离子切割机，并通过按钮将其归零。