# HTC Vive 给自主机器人指明了方向

> 原文：<https://hackaday.com/2016/08/23/htc-vive-gives-autonomous-robots-direction/>

HTC Vive 是一个虚拟现实系统，旨在与 Steam VR 配合使用。该系统试图超越耳机，通过使用两个基站在空间中跟踪耳机和控制器，使整个房间成为虚拟现实环境。硬件非常令人兴奋，因为它有潜力扩展游戏和其他虚拟现实体验，但它也已经显示出黑客的巨大潜力——在这种情况下是机器人定位和导航。

自主机器人通常利用两种基本方法中的一种来定位自己:机载传感器和地图来查看周围的世界(比如你在徒步旅行时如何确定方位)，或者房间中的传感器告诉机器人它在哪里(类似于你的 GPS 告诉你你在城市中的位置)。当然，每种方法都有其优缺点。如果你需要非常精确的位置数据，车载传感器传统上是昂贵的，而 GPS 位置数据太不精确，无法在比城市街道更小的范围内使用。

[Limor]立即在 [HTC Vive 中看到了解决这个问题的潜力](https://www.youtube.com/watch?v=1hiX0f6UAew)，至少对于室内应用来说是如此。使用 Vive Lighthouse 基站，他能够在三维空间中定位系统控制器，误差不超过 0.3 毫米。然后他能够在 Linux 系统上使用这些数据，并将其集成到 ROS ( [机器人操作系统](https://en.wikipedia.org/wiki/Robot_Operating_System))中。[Limor]还没有制造出利用这种方法的机器人，但显著的成本节约(一个完整的 Vive 需要 800 美元，但只需要灯塔和控制器)肯定会使这成为许多机器人制造商的理想选择。而且，正如我们已经看到的，[将 Vive 硬件与 DIY 电子产品](https://hackaday.com/2016/07/06/using-the-vives-lighthouse-with-diy-electronics/)集成应该是完全可能的。

 [https://www.youtube.com/embed/1hiX0f6UAew?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1hiX0f6UAew?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

