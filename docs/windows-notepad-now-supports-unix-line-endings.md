# Windows 记事本现在支持 Unix 行尾

> 原文：<https://hackaday.com/2018/05/08/windows-notepad-now-supports-unix-line-endings/>

这可能是本世纪最大的技术进步， [Windows 记事本现在支持 Unix 行尾](https://blogs.msdn.microsoft.com/commandline/2018/05/08/extended-eol-in-notepad/)。就这样了，各位。肯尼迪遇刺时你在哪里？尼尔·阿姆斯特朗踏上月球时，你在哪里？挑战者号爆炸时你在哪里？你现在在哪里*？*

以前，Windows 记事本仅支持 Windows 行尾字符—回车(CR)和换行(LF)。Unix 文本文档使用 LF 作为行尾，MAC 使用 CR 作为行尾。对于行尾人物来说，这种颠覆巴别塔的最终结果是一个可怕的混乱；Windows 用户无法在记事本中读取 Unix 文本文件，一切都太糟糕了。在 Windows 中打开一个 Unix 文本文件会产生一个没有任何空格的实心文本块。在任何其他地方打开一个 Windows 文本文件都会在每一行的末尾放置一个小矩形。

从当前的 Window 10 内部版本开始，记事本现在支持 Unix 行尾、Macintosh 行尾和 Windows 行尾。庆幸吧，技术上最大的问题现在已经解决了。