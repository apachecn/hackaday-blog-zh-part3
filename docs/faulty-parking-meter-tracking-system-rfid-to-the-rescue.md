# 停车计时器跟踪系统故障？RFID 拯救世界！

> 原文：<https://hackaday.com/2016/11/21/faulty-parking-meter-tracking-system-rfid-to-the-rescue/>

您多久发现一次需要解决的问题？你多久设计一次自己的解决方案——即使不会大规模实施？看到他的祖国斯里兰卡的许多市政停车场使用容易出故障的纸质票务系统，[Shazin Sadakath]想出了自己的解决方案:[一个高效的 RFID 标签记录系统](http://shazsterblog.blogspot.ca/2016/11/rfid-parking-solution-using-raspberry-pi.html)。

找出一个 HZ-1050 RFID 阅读器——以及一个 RFID 卡和两个标签——[Sada kath]开始将它连接到他的 Raspberry Pi，并编写一批代码和一个仪表板来工作。Python 脚本(使用 PiGPIO 库)读取 Wiegand 格式的 RFID 号码，并将其存储在 SQLite3 数据库中。Bootstrap、Javascript 和 JQuery trifecta 组成了仪表板，从所述服务器提取 RFID 信息，并将其组织成功能格式。

 [https://www.youtube.com/embed/L3eFGjyVWYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L3eFGjyVWYE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



像这样的 RFID 键控系统可能很难实现，即使是停车场的一小部分，但它仍然是一个潜在的解决方案。对于那些有类似计划的人来说，RFID 门禁系统无疑是办公室规模环境中的一个功能性解决方案。