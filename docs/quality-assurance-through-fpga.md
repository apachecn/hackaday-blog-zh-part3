# 通过 FPGA 实现质量保证

> 原文：<https://hackaday.com/2017/06/10/quality-assurance-through-fpga/>

康奈尔大学(Cornell)的[Bruce Land]ECE 5760 班的学生[Claire Chen]和[赵又廷]创建了一个针对制造业的项目:[通过视觉扫描一批产品并一次处理一个像素来自动检查制造产品的质量](http://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2017/yz424_clc288/yz424_clc288/final_website/index.html)。通常，小部件下线的时间是你必须请人来检查的时候。这个项目使用形态学图像处理，像膨胀和腐蚀来寻找瑕疵。

[Claire]和[Mark]创建了一条模拟生产线，通过伺服驱动带将一系列大礼包糖果带入摄像头的扫描范围。然后，带有 Cyclone V FPGA 和 ARM Cortex-9 的 SoC 处理原始图像以确定物体的颜色，同时通过一些算法来查找缺陷。FPGA 跟踪经过的狂欢次数及其颜色，以每秒 5-10 帧的速率保持 99%的成功率。FPGA 还将每个颜色块视为像素的集合，建立连接以帮助区分多个相互接触的狂欢。

另外，一定要看看[克莱尔]和[马克]上个学期的[自行车声纳](https://hackaday.com/2017/01/11/this-bike-sonar-is-off-the-chain/)项目。

 [https://www.youtube.com/embed/6QZgYuS9QR0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent](https://www.youtube.com/embed/6QZgYuS9QR0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=1&wmode=transparent)

