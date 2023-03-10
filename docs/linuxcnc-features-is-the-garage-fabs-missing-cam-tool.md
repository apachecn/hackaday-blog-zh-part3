# “LinuxCNC-Features”是车库制造厂缺少的 CAM 工具

> 原文：<https://hackaday.com/2015/12/25/linuxcnc-features-is-the-garage-fabs-missing-cam-tool/>

这需要一条很长的工具链，才能让这位未来的车库机械师通过所有需要的环节，开始生产零件。从选择 CAD 软件到将 3D 模型转换为 gcode 的 CAM 工具，再到咀嚼源代码并吐出*步*和*方向*脉冲来转动 cnc 铣床的曲柄的 gcode 解释器，有大量的开放和封闭源代码工具可供选择，甚至有机会开发一些我们自己的工具。这正是[尼克]和 cnc 俱乐部论坛上的人们所做的；他们[编写了他们自己的 CAM 工具](http://www.cnc-club.ru/wiki/index.php/LinuxCNC_Features)，使最终用户能够设计出可以导出到与 LinuxCNC 兼容的 gcode 的切削程序和刀具路径。

他们的工具被称为“LinuxCNC-features”，将一个与 LinuxCNC 兼容的图形 gcode 编程接口直接嵌入到 LinuxCNC 本地用户界面中。创建零件就是定义沿可编程刀具路径的连续切削列表。这些连续的切割是像钻孔、方形口袋、螺栓孔和线这样的处理。本机嵌入使机械师能够在 LinuxCNC 的实时视图中预览每个 3D 刀具路径，让他或她在运行之前快速检查以确保他们的 gcode 按预期执行。[Nick]有几个视频可以让你在你的[铣床](https://www.youtube.com/watch?v=giJUiZVTXas)或[车床](https://www.youtube.com/watch?v=fkOJhT69WEc)上运行。

LinuxCNC-features 已经问世近两年了，但是如果您想在车库里开始生产零件，就不要再寻找可以为简单项目快速生成 gcode 的 CAM 工具了。如果你不熟悉 LinuxCNC，它是最成熟的开源 gcode 解释器之一，旨在将你的 PC 变成 CNC 控制器，它是一些优秀的 DIY CNC 机器背后的大脑，比如这个[等离子切割机](https://hackaday.com/2014/06/27/linuxcnc-based-plasma-cutter-router/)。

 [https://www.youtube.com/embed/x7lQTTjvFXc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x7lQTTjvFXc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

