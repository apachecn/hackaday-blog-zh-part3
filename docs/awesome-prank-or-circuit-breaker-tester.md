# 可怕的恶作剧还是断路器测试？

> 原文：<https://hackaday.com/2017/01/31/awesome-prank-or-circuit-breaker-tester/>

许多工具既可以用来做好事，也可以用来做坏事——这只是取决于扳动开关的人。(以及他们目前的淘气程度。)我们在这里假定[Callan]是无辜的，并假设他[制造了他的远程控制剩余电流装置(RDC)跳闸器](https://callanbryant.co.uk/2015/02/02/rcdos_trip_the_power_from_your_phone_because_why_not/)，目的是测试他自己家中线路的安全性。另一方面，他确实提到在一次“无关的聚会倒计时”中，他用它关掉了家里的所有电源。看到了吗？善良的*和邪恶的*。

RCD(在美国称为 GFCI)是一种断路器，当火线和零线的电流量不相等且方向相反时，它就会跳闸，这表明电流在某处泄漏，希望不是通过某人。它们只需要几毫安的不平衡就能烧断，所以没人会受伤。制作测试 RCD 的设备很容易；hot 和保护接地电路之间的电阻即可。

[Callan]过度工程师。他使用了一个 50 W 的电阻，而在最坏的情况下 30 W 的电阻也可以。一个隐形的固态继电器在 Uno 和蓝牙模块的驱动下切换电阻器，因此他可以自然地从智能手机上断开断路器。

他*确实*在他的房子里发现了一个没有连接保护地线的电路，所以这个装置实现了它的安全功能。但它指出了这个项目作为恶作剧设备的一个弱点:毕竟，他只能朋克那些正确安装了断路器的人。相对于我们测试断路器的方式，这是一个相对安全的项目。但是，如果你对自己的电源安全实践不确定，请通读一下[我们关于电源电压的精美指南](http://hackaday.com/2016/05/11/looking-mains-voltage-in-the-eye-and-surviving-part-1/)。

 [https://www.youtube.com/embed/8_w1VXfULR4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/8_w1VXfULR4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

