# 黑客空间点唱机！

> 原文：<https://hackaday.com/2017/06/02/hackerspace-jukebox/>

根据你交谈的对象，音乐可能是完成工作不可或缺的一部分。在挪威特隆赫姆的 Hackheim hackerspace，Nikolai Ovesen 认为以前通过蓝牙播放音乐的系统背离了空间的协作和互动精神。解决方案:周末建造一个由树莓 Pi 驱动的自动点唱机。

点唱机只是用激光从胶合板上切割下来，然后用螺栓固定在一起。在内部，触摸屏使用双面胶安装，Raspberry Pi 3 和降压转换器通过主板垫片安装在其背面。IBM ThinkPad 电源线被重新设计和修改，以便通过降压转换器为放大器、Pi 和触摸屏供电。

一旦所有的东西都连接好、测试好、启动好，为了让 Golang 正常工作，就必须做一些巧妙的软件工作，还要设置触摸屏和放大器。黑客使用 Mopidy 音乐服务器及其 Mopify(Spotify)插件与点唱机进行互动，但他们也可以通过 Hackheim Slack 频道中的机器人点播歌曲。

 [https://www.youtube.com/embed/CNUYvNMBtsc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CNUYvNMBtsc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



所用代码的完整存储库在 [github](https://github.com/sosedoff/musicbot) 上，用于激光切割你自己的点唱机的文件…包厢，这里的[是](https://hackaday.io/project/24910/files)。

说到这个话题，乐高 CD 换碟机是否有资格成为点唱机？