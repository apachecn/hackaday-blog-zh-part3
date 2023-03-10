# 通过微控制器的 DAC 控制激光振镜

> 原文：<https://hackaday.com/2018/02/15/laser-galvo-control-via-microcontrollers-dac/>

镜式检流计(简称“检流计”)是激光投影仪的工作部件；他们能够非常快速准确地扭转镜子。利用其中的两个，激光束可以在 X 和 Y 方向上被操纵以形成图案。[bdring]购买了一些激光检流计，并决定[开发自己的控制系统](http://www.buildlog.net/blog/2018/02/laser-galvo-control-experiments/)，目标是用微控制器的 DAC(数模)输出驱动检流计。在那之后，让它画出一些形状所需要的只是一个激光和一个 3D 打印夹具来保持一切正确对齐。

galvos 配有驱动器来处理低级接口，【bdring】的工作是制作一个接口，将微控制器 DAC 的 0V–5V 输出范围转换为驱动器期望的 10 V 差分范围。他成功了，下面嵌入了一些测试模式的简短视频。

> [](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[在 Instagram 上查看此贴](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)[今晚在 NERP 玩我的激光电流计. .
> 
> @ [buildlog](https://www.instagram.com/buildlog/?utm_source=ig_embed&utm_campaign=loading) 在 <time style=" font-family:Arial,sans-serif; font-size:14px; line-height:17px;" datetime="2018-01-30T04:50:30+00:00">2018 年一月 29 日太平洋标准时间</time>晚上 8:50 分享的帖子](https://www.instagram.com/p/Bej48mcAaGY/?utm_source=ig_embed&utm_campaign=loading)