# 带 ESP8266 的连接计算器

> 原文：<https://hackaday.com/2017/04/29/the-connected-calculator-with-esp8266/>

计算器黑客已经存在了一段时间，我们已经看到了德州仪器 TI-83 和 TI-84 的大部分行动。当[johnkimdinh]找到一种方法来[给科学计算器](http://arduino.vn/tutorial/1563-phong-chong-nghe-thuat-hac-am-voi-esp8266-phan-4-thu-khoa-dai-hoc-co-kho) ( [机器翻译](https://translate.google.com/translate?sl=auto&tl=en&js=y&prev=_t&hl=en&ie=UTF-8&u=http%3A%2F%2Farduino.vn%2Ftutorial%2F1563-phong-chong-nghe-thuat-hac-am-voi-esp8266-phan-4-thu-khoa-dai-hoc-co-kho&edit-text=))添加一个 ESP8266 时，这一次是一个 Kenko FX-82M 计算器，它看起来与卡西欧 FX-82M 惊人地相似。

在他的视频中，[johnkimdinh]展示了他的黑客技术，它有一个向计算器传输数字的网络接口。这是通过使用 ESP8266 GPIOs 访问键盘来实现的，本质上相当于远程打字。电路的其余部分保持不变，所以更多的工作和其他功能应该可以远程使用。

也许这种技术最适合作为输出测量值和其他数据的专用显示器，这需要某种类型的后处理，以便人类可读。如果下一次迭代提供了从显示器上读取的能力，我们将真正取得进展。我们设想这种计算器将在未来的教育中使用，连接性将用于检索作业的一系列实时参数。在组合中添加一些传感器，这可能是 STEM 的下一件大事。

在过去，我们已经将[计算器应用于向量和矩阵数学](http://hackaday.com/2017/01/13/crippled-calculator-features-unlocked-with-automated-help/)以及连接到 TI-84 计算器的 [ESP8266s。毕竟大家都有计算器，简直要被黑！](http://hackaday.com/2016/05/02/who-needs-the-msp430-when-you-have-tis-other-microcontroller-the-ti-84/)

 [https://www.youtube.com/embed/Wmn9cgfd1vA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Wmn9cgfd1vA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

