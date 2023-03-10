# 学生着眼于 DIY 眼科检查

> 原文：<https://hackaday.com/2015/12/23/students-set-sights-on-diy-eye-exams/>

如果你能在家给自己做一个标准的视力检查会怎么样？这就是[乔尔、玛戈特和陈余]为[布鲁斯·兰德]的 ECE 4760 设计的最终项目背后的想法——模拟标准的斯内伦视力表，该视力表从 20 英尺的实际或模拟距离测试视力。

不过，这个测试有点不同。字母一个接一个地出现在 TFT 显示屏上，用户必须通过对着麦克风说话来识别每个字母。只要用户猜对了，系统就会显示越来越小的字母，直到达到相当于 Snellen 图表 20/20 线的大小。

由于该项目依赖于语音识别，该小组不得不考虑背景噪音和人声差异等因素。他们使用带通滤波器滤除人类声音范围之外的频率。为了确定说出的字母，PIC32 收集前 256 个和后 256 个样本，将它们存储在两个数组中，并对第一组执行 FFT。第二组样本进行 [Mel 转换](http://www.practicalcryptography.com/miscellaneous/machine-learning/guide-mel-frequency-cepstral-coefficients-mfccs/)，这有助于 PIC 对样本进行对数评估。最后，系统确定是否应该以相同的尺寸显示新的字母，以较小的尺寸显示新的字母，或者结束考试。

虽然这并不意味着取代由认证专业人员进行的视力检查，但这是一个有趣的项目，符合斯奈伦视力表的原则。唯一可能让这更好的是一个电子墨水显示器，让字母变得清晰。我们希望看到斯内伦的翻滚电子表格也能为还不认识字母表的孩子实现，尽管这可能需要一种完全不同的输入方法。休息之后，请务必观看演示视频。

不知道[布鲁斯·兰德]是谁？当然，他是康奈尔大学受人尊敬的高级讲师。但他在 hackaday . io 上也非常活跃[，有许多很棒的](https://hackaday.io/bruceland)[嵌入式工程讲座可以免费观看](http://hackaday.com/2015/12/21/microcontroller-lectures-by-bruce-land/)，每年我们都期待看到他的学生梦想并实现的项目，就像这个项目。你有自己的期末项目可以炫耀吗？不要羞于[发送提示](https://hackaday.com/submit-a-tip/)！

 [https://www.youtube.com/embed/LzhLs4Yyl9w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LzhLs4Yyl9w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

