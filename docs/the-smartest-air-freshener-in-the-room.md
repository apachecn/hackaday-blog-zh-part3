# 房间里最聪明的空气清新剂

> 原文：<https://hackaday.com/2017/12/16/the-smartest-air-freshener-in-the-room/>

许多自动空气清新剂很浪费，因为它们要么不停地喷洒房间，而手动的需要——嗯——手动操作。这在智能产品的时代是行不通的，所以 Instructables 用户[IgorF2]组装了一个空气清新剂，它不仅仅是在清新东西之前检查你是否在附近。

空气清新剂使用 NodeMCU LoLin 和 MG 995 伺服电机，NeoPixel 环充当状态灯。请注意，当伺服系统被触发时，电流会出现明显的尖峰，所以请确保您不是从 PC USB 端口或其他设备为空气清新剂供电。在 Fusion 360 中对空气清新剂的外壳进行建模后——文件可用[此处](http://www.instructables.com/id/IoT-Air-Freshner-with-NodeMCU-Arduino-IFTTT-and-Ad/#step1)——【Igor F2】将组件连接在一起，并将其安装在 3D 打印的外壳内。

硬件工作完成后，[IgorF2]详细介绍了如何为第一次使用的用户设置 Arduino IDE 和 ESP8266 支持，以及在草图中添加一些库。阿达果的组合。IO feed 和 ITTT——再次展示了设置步骤——处理空气清新剂的操作方式:位置检测、特定时间的喷洒，以及在那些特别懒散的时刻轻触手机上的软件按钮。

 [https://www.youtube.com/embed/IDUx2ac8V74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IDUx2ac8V74?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



[IgorF2]方便地提供并分解了他用来给观众中的新来者包装他的完整指令的代码。啊，一个完成的项目的香味。

如果你还不知道的话，家用空气清新剂也是一个零件宝库，可以用在许多地方，如 T2、T4、T5！