# 33C3:内存重复数据删除，黑客的朋友

> 原文：<https://hackaday.com/2017/02/04/33c3-memory-deduplication-the-hackers-friend/>

在第 33 届混沌通信大会上，[Antonio Barresi]和[Erik Bosman]提出了不是一个，不是两个，而是三个(3！！)伟大的黑客都基于[利用虚拟机中的内存重复数据删除](https://fahrplan.events.ccc.de/congress/2016/Fahrplan/events/8022.html)。如果你对安全感兴趣，你一定要看下面的演讲。抓住[滑梯](https://fahrplan.events.ccc.de/congress/2016/Fahrplan/system/event_attachments/attachments/000/003/152/original/33c3_memdedup_curse_slides_final.pdf)。(PDF)

对于大型虚拟机设置来说，内存重复数据删除是禁果——显然很危险，但却非常诱人。假设您正在托管虚拟机，并且您注意到许多机器同时在内存中有相同的内容。也许我们都在看同样的猫视频。他们只需存储 cat 视频的一个副本，并指向使用它的每台机器的共享内存块，就可以节省所有机器的全局内存。名义上独立的机器共享内存。什么会出错？

[![mem_dedup2](img/e8fe93e5e9f757e4d299fce9b09d706f.png)](https://hackaday.com/wp-content/uploads/2017/01/mem_dedup2.png) 基本上，去重后访问内存的时间会稍长，因为虚拟机必须查找自身以外的内存地址。如果攻击者有兴趣了解另一个虚拟机是否正在观看 cat 视频，他可以将 cat 视频放入他的内存中，等待虚拟机管理器对其进行重复数据删除，然后计算在他的内存中进行修改所需的时间。如果它比某个阈值长，则其他人正在观看猫视频。演讲的其余部分解释了对该漏洞的三种利用。

[CAIN 攻击](https://xorlab.com/blog/2015/07/30/cain/)允许攻击者计算出给定内存页面在相邻虚拟机中的地址。例如，想象一下 Windows DLL。基本思想如上所述，但是计算出内存页面中代码的偏移量是很困难的，但是他们通过在所有偏移量处编写相同的代码片段，并计算出哪一个匹配来强力执行。到目前为止，这种攻击只是泄漏了运行在另一个虚拟机上的程序的内存位置，但是可以把它看作是一个垫脚石。

第二次攻击增加了一个硬件漏洞，即[Rohm hammer 攻击](http://hackaday.com/2015/03/13/creative-dram-abuse-with-rowhammer/)，以利用运行在同一台机器上的进程。特别是，他们运行 Javascript 代码来利用微软的“安全”Edge 浏览器。他们使用内存重复数据删除攻击获得代码和堆指针的地址，创建代码对象，并使用 Rowhammer 将对象的地址转换为指针并运行它。这一切都归功于内存重复数据消除。

最后，“[翻转风水](http://www.vusec.net/projects/flip-feng-shui/)”通过破坏共享内存的本地副本将新数据写入受害者虚拟机，然后镜像回受害者。因为 Rowhammer 中的位翻转是不可预测但可重复的，所以第一步是找出位翻转的位置，然后在内存中对齐您希望在受害者虚拟机上更改的数据的副本。然后，内存被行锤击，因为它没有被明确地写入，过一会儿它可以渗透回受害者。

[![mem_dedup5](img/678490642a4e9ec4547e69a769ab0cda.png)](https://hackaday.com/wp-content/uploads/2017/01/mem_dedup5.png) 演示包括翻转受害者的 SSH 公钥中的几个位，使其变成一个容易分解的密钥，然后登录。在第二次攻击中，他们将密钥位翻转与拥有 web 域“ubunvu.com”相结合，使用其自动升级机制在受害者的虚拟机上安装任意软件。天啊。

这个演讲有时有点沉重，但其中的要点令人惊叹。“很明显”内存重复数据消除应该是一个问题，但实际上利用它(三种方法！)是绝技。他们没有说他们有责任，但值得注意的是，Windows 10 不再使用内存重复数据删除。

[https://media.ccc.de/v/33c3-8022-memory_deduplication_the_curse_that_keeps_on_giving/oembed](https://media.ccc.de/v/33c3-8022-memory_deduplication_the_curse_that_keeps_on_giving/oembed)