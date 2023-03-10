# 发带会根据你的心情点亮

> 原文：<https://hackaday.com/2015/12/07/hairband-lights-up-depending-on-your-mood/>

在学会了如何使用 ESP8266 之后，[Chirag Nagpal]决定做一个有趣的项目来试验从 Twitter 上收集数据。他称之为 [Sentiband](http://chiragnagpal.com/sentiband/) ，它会分析你最后一条推文的情绪，并相应地改变颜色。

有一个 API 叫做[sensition 140](http://help.sentiment140.com/home)(以前叫做“Twitter 情绪”)，它能够确定 Twitter 上一条推文的情绪内容。它使用机器学习构建的分类器，由斯坦福大学的几名计算机科学毕业生开发。我们以前见过它在[圣诞树装饰品上大规模使用，分析所有节日推特来点亮你的圣诞树。](http://hackaday.com/2013/12/25/christmas-tree-analyzes-your-tweets/)

[Chirag 的]版本允许你设置一个用户名，并显示隐藏在潜台词中的该用户推文的最新情绪。三个发光二极管亮起；绿色代表积极的推文，红色代表消极，蓝色代表中性。

显然，发带只是一个原型，但经过一点改进，我们可以看到它被用于一些互动的品牌发布会。

 [https://www.youtube.com/embed/fCl2-AIt0Eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fCl2-AIt0Eo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

