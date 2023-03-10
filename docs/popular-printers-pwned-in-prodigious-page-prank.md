# 受欢迎的打印机在巨大的页面恶作剧 pwn

> 原文：<https://hackaday.com/2017/02/04/popular-printers-pwned-in-prodigious-page-prank/>

新的一天开始了，我们又有了一个关于不安全网络设备的故事。这一次是所有品牌和描述的打印机引起了恐慌，因为[人们发现神秘的打印输出](https://www.reddit.com/r/hacking/comments/5rvfk7/another_one_popped_up_on_the_printer_at_work/)带有这样的信息:

" Stackoverflowin 回归了他的荣耀，你的打印机是僵尸网络的一部分，上帝回归了"

好吧，那就这样吧，你不能和神争论，尤其是一个显然已经用世界上的打印设备创造了一个僵尸网络的神。世界各地的打印机所有者自然担心他们的意外到来，并出现在支持论坛等场合表达他们的担忧。

我们当然习惯于相信打印机告诉我们的一切。墨水不足？我听到了，我无生命的复制朋友！但是当我们的打印机告诉我们这是僵尸网络的一部分时，也许是时候稍微思考一下了。完全有可能有人可以组装一个由受损打印机组成的僵尸网络，但在这种情况下，我们闻到了老鼠的味道。只有在滑稽的犯罪剧中，骗子才会以如此戏剧化的方式宣布他们的罪行，你可能会说这是僵尸网络*的*点*而不是*被其宿主检测到。阅读一些报告，似乎许多受影响的系统都向外界开放端口 9100，这是标准的 TCP 打印机端口，因此似乎更有可能是有人编写了一个小脚本，在端口 9100 打开的情况下查找 IP 地址，并使用此消息来欺骗他们。

这里真正的信息是我们期望 Hackaday 读者会非常熟悉的，并且我们在之前已经报道过[。许多网络连接设备很少考虑安全性，对于攻击者来说相对容易被击败。对于技术爱好者来说，解决方案相对简单，注意设备正在暴露哪些服务，锁定 uPNP 等服务，并关闭路由器上任何打开的端口。不幸的是，这些步骤可能超出了许多家庭用户，他们的路由器在他们的一生中都保持着默认的制造商设置。很遗憾我们的打印机巨魔没有添加](http://hackaday.com/2016/09/29/distributed-censorship-or-extortion-the-iot-vs-brian-krebs/)[基本路由器安全提示](http://www.makeuseof.com/tag/configure-router-make-home-network-really-secure/)的链接。

如果你想找点乐子，[一些打印出来的页面](https://www.reddit.com/r/hacking/comments/5rohyv/this_was_sitting_on_my_printer_tray_when_i_got/)包括[一个‘神’的电子邮件地址](https://www.reddit.com/r/hacking/comments/5rur11/apparently_mr_stackoverflowin_likes_us_because_we/)。弄清楚这是谁会很有趣，对吧？