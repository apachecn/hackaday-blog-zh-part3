# 用克隆征服地球

> 原文：<https://hackaday.com/2018/06/25/conquering-the-earth-with-cron/>

GOES-R 系列地球观测卫星是美国国家航空航天局提供的最新和最伟大的卫星。正如你所料，GOES-R 的部分工作描述是以高分辨率拍摄地球图像，但它们也具有实时照明监测以及增强的太阳耀斑和空间气象能力。这些全新的鸟类中，有四种将帮助我们关注地球到 21 世纪 30 年代的状况。花 110 亿美元还不错。

[![](img/8733e3661442b4aff31a2ef1ae23c2d7.png)](https://hackaday.com/wp-content/uploads/2018/06/goes_detail.jpg) 为了鼓励创新，美国宇航局通过与谷歌云平台的合作，将 GOES-R 卫星收集的图像公之于众。[本·尼特金]决定研究这些数据，并开发了[一个互动网站，让你从 GOES-R](http://bluemarble.nitk.in)的视角来可视化地球。但是不要让这些漂亮的视觉效果欺骗了你，这个网站是由一些 cron jobs 和一些静态 HTML 驱动的。正如蒂姆·伯纳斯·李爵士所愿。

但是这不像调度一个`wget`命令那么容易；GOES-R 收集的图像被分成不同的波长，需要组合在一起才能产生假彩色图像。一个 cron 作业每五分钟启动一次，下载并合并原始 GOES-R 图像，然后另一个 cron 作业启动一个 Python 脚本，使用 ffmpeg 从图像中创建 WebM 延时视频。所有的 Python 脚本和 crontab 文件[都可以在 GitHub](https://github.com/bnitkin/goesr-video) 上获得。

最后，随着图像的合并和视频的创建，静态 HTML 网站通过一个快速而肮脏的 Python web 服务器呈现在世人面前。该网站可以通过更传统的方式提供服务，但[本]喜欢尽可能降低管理费用。

如果你想走更直接的路线，我们已经介绍了大量专注于从气象卫星上下载图像的项目；[从使用老派的【兔耳】](https://hackaday.com/2017/07/10/old-rabbit-ears-optimized-for-weather-satellite-downlink/)到[解码最新的俄罗斯流星-M N2](https://hackaday.com/2017/12/05/grabbing-raw-images-from-a-new-russian-satellite/) 下行。

 [https://www.youtube.com/embed/6Q7Leqvzfg4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6Q7Leqvzfg4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

