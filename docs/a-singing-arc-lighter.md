# 一个会唱歌的弧光灯

> 原文：<https://hackaday.com/2017/01/02/a-singing-arc-lighter/>

我们都有过买我们想要但不需要的东西的罪过。多亏了那些提供廉价商品的远东网站，[PodeCoet]就是这样发现自己拥有了几个双电弧电动打火机。这毕竟是给予的季节，理应如此。作为一名黑客，显而易见的事情就是让他们发出刺耳的声音。如果你还拿着你的气体打火机，不要——因为这些电动打火机“太容易被破解了”。双弧是一样的，但乐趣是两倍。

[PodeCoet]从拆下打火机开始，找出[原理图](http://ultrakeet.com.au/uploads/arcLighter/schematic.jpg)并了解其工作原理。有一个用于 LiPo 的充电器 IC，一个无法识别的微控制器，一对驱动一对功率晶体管的 FET，这反过来驱动大约 15.6kHz 的 HF 输出变压器。他猜测“原始微控制器可能是像 12C508 一样的 OTP 部件”，但在没有 chipID 的情况下，他不能确定。

他没有为此伤透脑筋，而是换了一个引脚兼容的 PIC12F1840。剩下要做的就是写一些 quick-n-dirty 代码，[用有趣的注释](http://ultrakeet.com.au/uploads/arcLighter/main.c)来点缀它，以便在音频上调制输出信号。他的第一首曲子是冰岛教育音乐喜剧儿童电视连续剧《懒惰镇》的《我们是第一》。但是[的 redditors](https://www.reddit.com/r/electronics/comments/5kq3hy/arc_lighter_modified_to_play_a_tune_by_modulating/) 很牛逼，有人要求他加上“帝国进行曲”，【PodeCoet】答应了。

由于他要赠送这些打火机，这个鬼鬼祟祟的黑客在代码里加了一个恶作剧。每次按下按钮超过两秒钟，它就会正常工作，计数器就会增加。数到 20 的时候，曲子就开始了，仅此一次。无论按多少次按钮都不会再播放这首曲子，让用户困惑，怀疑自己是否产生了幻觉。这也有助于确保打火机不会过早自毁，因为输出变压器可能是为低占空比设计的。他的博客帖子包含了进行这种黑客攻击所需的所有信息，以及避免他所面临的问题的便利技巧。我们认为，当点燃生日蜡烛时，一首“生日快乐”的曲子会很棒。

[PodeCoet]喜欢高压的东西——看看“[自制电棍让你从拆迁员变成警察](http://hackaday.com/2013/01/07/home-built-stun-baton-turns-you-into-a-cop-from-demolition-man/)”。这个人肯定喜欢他的恶作剧，正如“[黑掉你同事的标签制造商](http://hackaday.com/2015/01/25/hacking-your-coworkers-label-makers/)”所证明的。这出闹剧非常精彩——“[学生流氓反 Arduino 教授与寄生虫 MCU](http://hackaday.com/2014/12/25/student-trolls-anti-arduino-prof-with-parasite-mcu/) ”。

 [https://www.youtube.com/embed/9tyEg218Jqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9tyEg218Jqg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



 [https://www.youtube.com/embed/p8cwIA50DOY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p8cwIA50DOY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



感谢[ryg]向我们透露了 reddit 主题。