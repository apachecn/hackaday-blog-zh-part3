# 自动 MtG 卡片分类器将破烂与财富分开

> 原文：<https://hackaday.com/2018/05/17/automatic-mtg-card-sorter-separates-rags-from-riches/>

像我们许多人一样，[迈克尔·波特拉]小时候是一个狂热的交易卡收藏家。也像我们许多人一样，生活妨碍了我们，这些收藏品被放在盒子里无人问津，直到我们的母亲威胁要扔掉它们(或者干脆跳过威胁，在车库拍卖中以近乎零的价格卖掉它们)。

[迈克尔]最近与他收集的魔法卡片重聚，这些卡片的价值不亚于棒球或任何其他种类的收藏卡片。既然他的周五晚上都被别人占了，他决定卖掉它们。但首先，他必须知道它们值多少钱。

手动对数百张卡片进行分类和定价所花费的时间比他希望的要长，所以[他建造了一个分类器来自动化这个过程](https://www.hackster.io/mportatoes/trading-card-scanner-organizer-84399a)。它需要一叠 MtG 卡，并使用伺服系统和小轮胎将它们一个接一个地移动到位。一个简短的 Python 脚本运行伺服系统，告诉 Raspi 3 相机拍摄每个镜头，并上传到亚马逊 AWS。一旦有了图片，[Michael]使用第二个脚本从图片中获取卡片标题文本，并通过 TCGPlayer 的定价 API 获取值。

这台机器可能不适合纯粹主义者或有一堆同一张卡片的原件和再版的人。我们可能应该提到，他首先拿出了所有的黑莲花和其他明显有价值的卡。仍然需要有人评估每张卡的状况，但是每张卡两秒钟，这是相当节省时间的。时间走过休息，看看它在行动。

厌倦了使用骰子或草稿纸作为你的生命计数器？召唤一些谢妮管，做一个更酷的。

 [https://www.youtube.com/embed/L8qgvaLiFcc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/L8qgvaLiFcc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



Via [ [r/raspberrypi](https://www.reddit.com/r/raspberry_pi/comments/8jupqe/a_machine_that_automatically_scans_and_retrieves/)