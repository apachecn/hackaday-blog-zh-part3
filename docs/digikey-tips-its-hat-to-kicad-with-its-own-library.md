# Digikey 用自己的库向 Kicad 脱帽致敬

> 原文：<https://hackaday.com/2018/05/01/digikey-tips-its-hat-to-kicad-with-its-own-library/>

Digikey 可能会以其庞大的库存让我们惊叹，但现在他们以个人姿态让我们惊叹。这家总部位于美国的电子产品供应商对拥有自己的[零件库](https://forum.digikey.com/t/the-what-and-why-of-digi-key-kicad-library/1345)的 KiCad 用户点头表示赞同。更重要的是，[【克里斯·甘梅尔】向我们展示了它最初的主要特点](https://www.youtube.com/watch?time_continue=53&v=o44Z6sUbuIo)和背后的思考过程。

随着所有工作进入这个库，很高兴看到 Digikey 对 KiCad 进行了彻底的研究，以及它如何适应开源 PCBA 设计的现状。首先，这个库遵循与大多数其他 KiCad 库略有不同的设计模式，因为它是一个*原子零件库*。这意味着每个符号都与特定的制造商零件号相关联，因此也与特定的封装外形相关联。虽然这种风格反映了 EagleCad 的；KiCad 库通常将符号与示意图分开，以便符号可以重复使用，零件可以更容易地在 BOM 中交换。这里没有“最佳”实践，所以 Digikey 的人认为他们应该公开第二种选择。

下一步，这个库已经有将近 1000 个部件，并且还会继续增长。这些不仅仅是 Yageo 电阻库存的完整系列。他们实际上是从 Seeed Studio 的[开放零件库](https://www.seeedstudio.com/opl.html)中的零件开始培养他们的零件库的。这些是业余爱好者可能实际使用的组件，因为一些组装服务有一个工作流，使用这些部件的设计移动更快。最后，由于所有零件都有特定的供应商零件号，BOM 上传到在线购物车更方便，使 Digikey 更容易向我们索要零件。

是的，反对者可能仍然会在这个新图书馆的基础上呼喊“利润”或“资本主义”，但从这个项目的努力来看，这是 Digikey 的一个温暖的姿态，为爱好者带来了大量积极的个人笔记。最后，我们仍然可以从这个项目中的大量工作中受益——即使我们没有按预期使用它。[许可许可](https://github.com/digikey/digikey-kicad-library/blob/master/LICENSE.md)允许我们抓取符号，并按照我们喜欢的方式重用它们。(事实上，对于目光敏锐的法律专家来说，他们实际上明确废除了衍生项目不需要获得知识共享许可的条款。)

随着来自像 Digikey 这样的大供应商的成熟的社区支持，我们更加渴望得到 KiCad V T1。

 [https://www.youtube.com/embed/o44Z6sUbuIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o44Z6sUbuIo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)



谢谢你的提示，[戴夫]！