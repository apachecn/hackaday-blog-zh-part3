# 数字传输模拟电视

> 原文：<https://hackaday.com/2016/10/05/transmitting-analog-tv-digitally/>

如果你想真正理解一项技术，如果你像我们一样，你需要自己重新构建它。通过阅读维基百科，甚至通过查看示波器描迹，说你理解(模拟)广播电视是一回事。但是当你写了一个流程图，仅仅使用软件定义的无线电成功地[将测试图像传输到普通电视](https://hackaday.io/project/14904-analog-tv-broadcast-of-the-new-age)时，你可以很容易地说你已经掌握了这个主题。

![9944491474271463115_thumbnail](img/0e4e48e702af3123d9984e3badf66f97.png)[Marble]为 PAL 编写了他的 flow，但是如果你住在美国或日本，修改它以与 NTSC 兼容应该是相当容易的。发送黑白图像很“简单”,但是要传输全彩色图像，你需要了解色彩空间。查看一下【大理石】的[项目日志](https://hackaday.io/project/14904/logs)。

Hackaday 还有另一个对恐龙电视广播感兴趣的黑客:[CNLohr]。看看他为 attini 和 ESP8266 打造的[和](http://hackaday.com/2015/02/26/attiny85-does-over-the-air-ntsc/)[。](http://hackaday.com/2016/03/01/color-tv-broadcasts-are-esp8266s-newest-trick/)

(是的，头条图片是~~他早期的黑白试验~~之一，来自[维基百科](https://en.wikipedia.org/wiki/Scan_line)——我们只是喜欢它的外观。)