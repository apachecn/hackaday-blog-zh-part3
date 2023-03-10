# 3000W 独轮车唯一的限制就是“个人勇气”

> 原文：<https://hackaday.com/2018/04/23/3000w-unicycles-only-limitation-is-personal-courage/>

[![](img/151caaaa52af8e46f79f02a0434be068.png)](https://hackaday.com/wp-content/uploads/2018/04/3000w-unicycle-square-anim.gif) 电动汽车是创新的沃土，因为合适的电机、控制器和电源的可用性使得即使是业余爱好者也可以进行实验。即便如此，[约翰·丁利]自 2009 年以来一直在研究这种车辆，他的最新自平衡电动独轮车确实将标准提高了多个等级。它拥有一个巨大的 3000 瓦无刷轮毂电机，旨在用于电动摩托车，而[约翰]能够利用剩余的飞机和摩托车零件添加许多触摸功能，如语音反馈和 1950 年代的造型。为了转向，车架在车把的帮助下稍微改变形状，以允许驾驶员的重心向车轮的一个或另一个外缘转移。在一个废弃的海滩试驾中，[约翰]告诉我们，自行车从未超过 20%的功率；设备的局限性完全靠个人勇气。观看下面嵌入的测试视频。

 [https://www.youtube.com/embed/CE0rmpAKH4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CE0rmpAKH4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



我们介绍了[【约翰】以前的独轮车](https://hackaday.com/2016/06/09/self-balancing-one-wheeled-motorcycle-tears-up-the-beach/)，它使用了 DC 电机和链传动；限制无刷轮毂电机使用的主要因素是合适的速度控制器的可用性。在自平衡车中使用时，速度控制器必须在前进和后退方向都提供稳定的控制，但大多数都设置为仅向前行驶。[John]找到了一种为电动船设计的速度控制器形式的解决方案，但仍然需要做一些集成工作，通过手工焊接 LTC2644 DAC 将 PWM 转换为平滑的模拟电压。电力来自轮子上方圆柱形机身中的二十个磷酸铁锂电池，开关和旋钮提供控制软件的微调。由于该建筑缺乏任何类型的数字显示，使用来自彼得·奈特的[有声图书馆](https://github.com/going-digital/Talkie)的 Arduino 提供了 80 年代风格的计算机语音，向司机讲述警报和状态。尽管像电机和速度控制器这样的组件是使构建成为可能的关键部分，但仍然需要大量的集成和软件工作。

[约翰]真的知道他的东西；他有一个关于自动平衡车的资源页面，这里有一个关于最新独轮车建造过程的 T2 YouTube 播放列表的链接。干得好！