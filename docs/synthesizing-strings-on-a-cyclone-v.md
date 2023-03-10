# 在 Cyclone V 上合成琴弦

> 原文：<https://hackaday.com/2017/05/18/synthesizing-strings-on-a-cyclone-v/>

康奈尔大学的学生[Erissa]、[Albert Xu]和[Sophia Yan]建造了一个[FPGA 波动方程音乐合成器](http://people.ece.cornell.edu/land/courses/ece5760/FinalProjects/s2017/eli8_sjy33_awx2/ece5760finalproject/ece5760finalproject/index.html)，作为[Bruce Land]的[ECE 5760](http://people.ece.cornell.edu/land/courses/ece5760/)课程的最终项目。

该团队使用 [Kaplus-Strong 弦乐合成](https://en.wikipedia.org/wiki/Karplus%E2%80%93Strong_string_synthesis)方法设计了一个由 Cyclone V FPGA 演奏的四弦乐器三重奏。在开发板的 ARM 9 HPS 上运行的 C 程序充当音乐序列器，控制节奏并告诉 FPGA 播放哪个音符。

学生们创作了四首歌曲的版本，包括波卡汉塔斯配乐的《风的颜色》、《远在卡尤加的水域之上》(康乃尔的母校)和约翰·传奇的《我的全部》。一个简单的 GUI 允许观众选择一首歌曲，并选择演奏哪种或哪些乐器，为每首歌曲提供多种变化。

谢谢，[ [布鲁斯](https://hackaday.io/bruceland)！

 [https://www.youtube.com/embed/DvpA_gBL1VU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/DvpA_gBL1VU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

