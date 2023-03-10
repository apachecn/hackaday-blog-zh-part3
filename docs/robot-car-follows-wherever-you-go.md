# 无论你去哪里，机器人汽车都会跟着你

> 原文：<https://hackaday.com/2017/07/20/robot-car-follows-wherever-you-go/>

在一天结束的时候，养一只宠物真的会给你的快乐带来很大的不同，但是它们也是很大的工作量。(约安尼斯·斯托尔蒂迪斯)的这个项目做了类似的事情——去掉了所有的责任。[智能汽车跟随者项目](http://arch.icte.uowm.gr/projects/smart_car2017/)旨在使用蓝牙和红外跟踪人们，并跟随他们从一个房间到另一个房间。

作为硕士论文的一部分提交，这个项目破解了一辆玩具汽车，并使用钥匙链发射器来发送跟踪信号。Raspberry Pi 3 结合了蓝牙 RSSI 和红外信号来估计信标的位置。Arduinos 有助于红外信号和电机控制，允许机器人像小狗一样追逐用户。整件事还附带了使用超声波传感器的避障功能，如果你的房子里有很多家具，这是很好的。

你也可以选择手动模式，用电脑和游戏手柄来驾驶它。连接到车载计算机的网络摄像头通过 wifi 向 PC 应用程序发送视频，以第一人称观看车辆。OpenCV 用于创建最终的 GUI，允许您远程查看和控制项目。任何想要复制这个项目的人都可以下载源代码。看看下面的视频吧。

OpenCV 的使用意味着该设计可以在以后重复使用来制造具有视觉的机器人。Raspberry Pi 已经被证明是一个强大的图像处理平台，但是如果你需要额外的能力，这个项目可能是一个很好的起点。对于 OpenCV 更有野心的应用，看看这个[激光射击机器人](http://hackaday.com/2017/04/18/robot-targets-eyeballs-fires-lasers-oshas-gonna-love-this-one/)。

 <http://arch.icte.uowm.gr/projects/smart_car2017/video/smart_car_full_sort.mp4?_=1>

[http://arch.icte.uowm.gr/projects/smart_car2017/video/smart_car_full_sort.mp4](http://arch.icte.uowm.gr/projects/smart_car2017/video/smart_car_full_sort.mp4)