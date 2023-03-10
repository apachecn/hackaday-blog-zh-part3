# DIY 光学传感器分线板制作 DIY 光学鼠标

> 原文：<https://hackaday.com/2016/11/21/diy-optical-sensor-breakout-board-makes-diy-optical-mouse/>

想要尝试使用光学鼠标传感器，但对缺乏选择感到有点沮丧，[Tom Wiggins] [为 ADNS 3050 光学鼠标传感器](https://hackaday.io/project/18344-adns-3050-optical-sensor-mouse)推出了自己的分线板，并在开发过程中使用它来制作自己的 3D 打印光学鼠标。光学鼠标传感器本质上是跟踪运动并将其提供给主机的独立相机。为了正常工作，传感器需要一个透镜组件和适当的照明，这两者都与传感器一起配合到一个专门的支架上。[Tom]找到了原始 ADNS LED 的替代品，但仍然找不到传感器支架，所以他自己设计了一个。

[![optical-mouse-sensor-breakout-square](img/9afac9a31d9e9fbd5586053c8c563214.png)](https://hackaday.com/wp-content/uploads/2016/11/optical-mouse-sensor-breakout-square.jpg)[github 库](https://github.com/Tom101222/Adns-3050-Optical-Sensor)包含所有的设计文件以及 Arduino 库。考虑到其他人可能会和他一样对 ADNS 3050 的易用分线板感兴趣，该分线板兼作安装支架，[Tom]在 Kickstarter 上发起了一场小规模生产活动。

光学鼠标传感器经常在 hobby robotics 中作为实验性运动跟踪器出现，甚至作为低分辨率摄像机出现在 T2。这些小软件包中有很多内容，[Tom]的完全文档化的开源设计试图让它更易于访问。