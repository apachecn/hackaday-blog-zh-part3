# Android 机顶盒允许您通过 HDMI 输入进行流式传输和录制

> 原文：<https://hackaday.com/2016/01/06/android-set-top-box-lets-you-stream-and-record-via-hdmi-input/>

在寻找可以通过局域网传输视频的硬件时，[danman]得到了一个建议，可以试试€69 Tronsmart Pavo M9(他指出这是一个重新命名的 Zidoo X9)。通过一些方便的 Linux 终端工作和一些关键的软件,[danman]能够做到这一点。

正如[danman] [在他的博客](https://blog.danman.eu/using-tronsmart-pavo-m9-for-hdmi-input-streaming/)中解释的那样，Android box 能够通过主菜单中的预装软件从 HDMI 输入端录制视频。文件格式选项在记录菜单中可用，但是没有一个适合视频流(这是目标，记得吗？).

[danman]能够轻松地检查系统，因为这些盒子都是出厂时安装的(或者至少是[danman]在演示中使用的 Tronsmart 版本)。任何拥有 Zidoo X9 的人都可以验证对根目录的访问吗？

长话短说，[丹曼]能够让流在网络上工作。尽管他确实需要对通过 ssh 发出的 stream 命令进行一些修改。他在 ffmpeg 文档中找到了修复方法，省去了通读的麻烦，但是你必须查看他的博客文章(专业提示:他链接到一个可爱的小。apk 逆向工程工具)。

我们以前见过机顶盒黑客，然而，以这个价格传输和录制 HDMI 是一个罕见的发现。如果你一直在砍同一棵树，请在评论中告诉我们，别忘了[发送那些提示](http://hackaday.com/submit-a-tip/)！