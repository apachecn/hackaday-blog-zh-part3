# 遥控汽车赛车圣诞树和速度陷阱

> 原文：<https://hackaday.com/2016/09/20/rc-drag-racing-christmas-tree-and-speed-trap/>

在飙车界，圣诞树是起跑线上的柱子，依次点亮一组黄灯，紧接着是绿灯，告诉车手们出发，这些灯显然给了它季节性的名字。在树的底部有激光来探测汽车的存在。

[迈克]不仅为他的遥控车制作了他自己的圣诞树，而且他甚至制作了一个轨道终点电路，用 LED 显示屏告诉这些车花了多长时间。开始和结束硬件都由 [Pololu Wixel 板](https://www.pololu.com/product/1336)控制，该板具有 TI CC2511F32 微控制器，内置 2.4 GHz 无线电用于无线通信。

除了发光二极管，圣诞树上还有一束激光束，使用一个 650 纳米的红色激光二极管为起跑线上的每辆车瞄准一个 [TEPT5600 光电晶体管](https://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=1108144)。如果一辆车在绿灯前穿过它的光束，那么红灯就表示这辆车被取消资格。

轨道终点电路有 7 段显示每辆车的时间。[Mike]设计了该系统，以便圣诞树的微控制器告诉轨道末端电路的微控制器何时重置时间、启动时间以及在不合格的情况下清除时间。终点线控制器有激光器和光电晶体管，就像起跑线一样停止计时器。

哦，我们有没有提到他还加入了 1980 年赛车游戏的声音？休息之后，请观看视频，了解所有活动。如果汽车看起来有点醉了，那是因为在控制器上向左或向右推会使方向盘完全向左或向右。

 [https://www.youtube.com/embed/JwOyFHUCe60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JwOyFHUCe60?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

