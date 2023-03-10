# 硕士无人机项目起飞

> 原文：<https://hackaday.com/2016/06/17/masters-uav-project-takes-flight/>

来自波兰弗罗茨瓦夫斯卡理工学院的[Przemyslaw Brudny]、[Marek Ulita]和[Maciej Olejnik]为他们的论文项目打包了一架装满定制传感器板的无人机。

天行者 X-8 FPV 无人机经历了广泛的修改，以适应嵌入式系统，并升级了碳玻璃底盘，以承受他们进行测试所需的高负载和速度。副翼是为了更好地控制无人机而定制的。但对我们来说，支持这些传感器的所有电路板设计才是真正有趣的。

许多系统由两块恩智浦 Kinetis K66 板支持，这两块板构成了无人机的主干，一块作为飞行系统的控制器，另一块作为传感器和电源控制板。传感器板拥有三个恩智浦 MPL3115 气压传感器、一个恩智浦 FXOS8700CQ 3D 加速度计、恩智浦 FXAS21002C 陀螺仪以及 WiFi 和 GSM 卡。

在另一项工程实力的壮举中，一个专门构建的编程和调试板允许通过一根专用电缆访问 Kinetis K66 板。

[![Complete model with electronics, batteries, motors and sensor carbon tubes](img/3d904ecb5e1f781700c43d599754ad14.png)](https://hackaday.com/wp-content/uploads/2016/06/prograrmming-the-firmware.png)

最终产品是一架几乎完全定制的无人机，展示了这三名研究生的技能，证明了你确实可以主修无人机。随着应用的多样化，例如农业，对无人机和无人驾驶飞机面临的技术障碍的巧妙解决方案的需求意味着毕业生积累的技能将在短期内受到高度需求。