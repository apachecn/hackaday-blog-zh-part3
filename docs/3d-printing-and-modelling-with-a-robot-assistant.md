# 使用机器人助手进行 3D 打印和建模

> 原文：<https://hackaday.com/2018/03/20/3d-printing-and-modelling-with-a-robot-assistant/>

[胡爱书·彭]和一群其他研究人员已经开发出一个系统，允许他们使用虚拟现实(VR)在他们面前的空间中建模一个对象，同时机器人在同一空间中 3D 打印该对象，这是一个真正的合作努力，他们称之为 [RoMA:机器人建模助理](http://www.huaishu.me/projects/roma.html)。这是解决设计问题的一个步骤，然后必须等待原型制作完成，才能知道它是否符合设计目标。

![The parts: designer, AR headset, AR controller, rotating platform, robotic printer](img/c1eb2f1268931cb9fcc145167a96440f.png)

The parts

设计师/机器人协作是如何工作的？设计师戴着一个 Oculus Rift VR 头戴设备，前面安装了一个摄像头，将其变成了一个 AR(增强现实)头戴设备。设计师面前是一个旋转平台，物体将在上面进行 3D 打印。平台的另一边是 3D 打印机器人。在 AR 头戴式耳机中，设计师通过相机查看平台、物体和机器人，但他正在处理的模型覆盖在物体上。AR 手控制器允许他在模型上工作。同时，机器人 3D 打印模型。请观看下面的视频。

下面的视频通过设计和打印一个茶壶展示了这种合作的一些优势。当需要为茶壶的手柄建模时，设计师伸出手，将手指放在应该穿过手柄的地方，同时在手指周围画一个虚拟手柄。这样就不太可能打印出一个带把手的完整茶壶，却发现把手不够大。

他们还展示了如何将物理对象放在平台上，然后在对象上进行绘制和 3D 打印。在下面的视频中，他们给玩具喷气式战斗机添加了一个支架。或者你可以稍微绘制和 3D 打印，然后添加物理对象进行缩放，然后甚至在它们周围绘制和 3D 打印。他们在关于这个项目的论文中展示了这一点[,他们围绕一些乐高积木创建了一个结构。](http://www.huaishu.me/projects/roma.pdf)

与任何协作一样，他们必须制定一些基本规则，他们称之为域，控制谁可以在不同时间访问对象。例如，当设计者靠近平台时，机器人可以在平台的一侧进行打印，但如果设计者接触到平台，机器人会自动后退。如果设计者离平台很远，那么机器人可以做任何它想做的事情，包括旋转平台。

与工业级机械臂共享一个工作空间可能是危险的。除了这些领域，机器人手臂被编程为保持在其工作区域，如果设计者误入机器人的工作区域，那么手控制器就会振动。机器人的速度也受到限制。

正如你所料，他们还编写了一些软件，一个 AR 渲染器和一个 AR 编辑器，但我们将把这些留给他们的论文来描述。

如果这看起来很熟悉，那可能是因为他们之前的动态打印让我们惊叹不已，这是这个正在进行的项目的第一次迭代。

 [https://www.youtube.com/embed/K_wWuYD1Fkg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K_wWuYD1Fkg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

