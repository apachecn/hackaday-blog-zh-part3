# 公民瓦特和社区的力量

> 原文：<https://hackaday.com/2016/03/15/citizenwatt-and-the-power-of-community/>

取决于你生活在世界的哪个地方，你的国家或地方政府，或你的公用事业公司，有可能把智能电表列入他们的议事日程。这个想法是，这些连接到网络的能源计量表将允许您更好地控制能源使用，并通过更有效地利用能源来降低成本。大胆的计划已经提出，电表可以控制你的大功率电器，如热水器、洗衣机或家庭供暖系统，能够根据一天中的时间、能源的现货价格或整个电网的负荷来关闭或打开它们。

然而，这些设备并非没有争议。例如，隐私问题集中在从个人收集的数据中可以收集到的个人信息的数量上。或者说安全性，安装在数百万家庭并控制大功率电器的联网电子设备中的漏洞如果被成功利用，可能是灾难性的。

在巴黎的一个小区域，他们正试图为一个没有这些风险的社区获得智能电表的一些好处。 [CitizenWatt](http://www.citizenwatt.paris/) (法语， [谷歌翻译链接](http://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.com&sl=auto&tl=en&u=http://www.citizenwatt.paris/&usg=ALkJrhgg493GMu9ITqJGW6rYrTfCgzHxrw))是一个开源的智能能源监控器，它提供了智能电表的一些好处，同时允许其所有者保留对其生成的数据的控制，只在他们同意的情况下共享数据。整个项目诞生于[Citoyens captures](http://www.citoyenscapteurs.net/)(公民传感器、法语、[谷歌翻译链接](http://translate.google.com/translate?hl=&sl=fr&tl=en&u=http%3A%2F%2Fwww.citoyenscapteurs.net%2F))[hackEns](https://hackens.org/)(法语、[谷歌翻译链接](http://translate.google.com/translate?sl=auto&tl=en&u=https%3A%2F%2Fhackens.org%2F) ) hackspace、 [Fabelier](http://fabelier.org/) FabLab 和巴黎市之间的关联。

CitizenWatt 系统包括一个电力传感器和一个基站。该传感器是一种简单的电池供电设备，它从夹在供电电缆上的电流互感器中获取输出，并通过 ATMEGA8 微控制器将其馈送到 2.4GHz 射频链路。基站是一个 Raspberry Pi，它从 RF 中检索数据，存储数据，并允许用户通过 web 界面查看数据。[传感器代码和硬件文件](https://github.com/CitoyensCapteurs/CitizenWatt-sensor)，以及树莓 Pi 基站的[文件](https://github.com/CitoyensCapteurs/CitizenWatt-Base)都可以在 GitHub 上免费获得。

为了保持项目的开放性，CitizenWatt 团队组织了一系列活动，在这些活动中，参与巴黎郊区试验的家庭有机会制作自己的传感器板，其中许多人都是第一次接触烙铁。

这些年来，我们已经在这些页面上看到了不少智能电表。有[这个基于 Spark 核](http://hackaday.com/2015/07/11/non-invasive-smart-electricity-meter/)，这个[基于 ESP8266](http://hackaday.com/2014/11/02/an-esp8266-based-smartmeter/) ，还有[这个由公用事业公司](http://hackaday.com/2010/09/18/smart-power-meter-interface-for-the-linux-crowd/)提供，数据可以访问。CitizenWatt 是一个值得加入他们的项目，但它让当地非制造商社区参与进来，这是它与众不同的地方。我们应用了这个项目的这个方面，我们希望我们能看到更多这样的项目。