# 用 OpenSCAD 制作橡皮图章

> 原文：<https://hackaday.com/2017/12/10/making-rubber-stamps-with-openscad/>

有一句老话是这么说的“如果你不能打败他们，就加入他们”，但在这些地方，一个更好的版本可能是“如果你不能买他们，就制造他们”。相当大一部分美化了这些页面的项目是黑客或制造商的产品，他们无法找到符合他们需求的商业产品。或者至少，找不到一个符合他们预算的。

GitHub 用户[harout]想买一些橡皮图章来帮助孩子们学习亚美尼亚字母，但是找不到一套可以买到的橡皮图章。凭借一台 3D 打印机和一些 OpenSCAD 代码 , [harout]能够将这个商业上的缺点变成一个 DIY 的成功故事。

[![](img/457487152b26b3a40b7aab6c945c7e7c.png)](https://hackaday.com/wp-content/uploads/2017/12/diystamp_detail.jpg)

Filling the molds with urethane rubber.

他不需要手动渲染每个图章，而是能够编写一个简单的 [Bash 脚本，用“-D”选项](https://github.com/harout/alphabet-stamps/blob/master/build.sh)调用 OpenSCAD。当这个选项被传递给 OpenSCAD 时，它允许您在。scad 文件。因此，单个 OpenSCAD 文件能够为命令行上传递给它的任何字母创建一个戳记。Bash 脚本使用这个选项来更改保存字母的变量，将 STL 呈现为一个惟一的文件名，然后移动到下一个字母并重复这个过程。

STLs 的这种过程化生成是对 OpenSCAD 的奇妙使用，当然不仅限于简单的儿童邮票。通过对代码的一些改进，该脚本可以接受任何给定的字符串和字体，并生成一个准备打印的模型。

随着全套字母模具的生成，它们可以被打印出来，并用丙烯酸喷漆密封。对每个密封模具使用脱模剂，最后用大约 200 毫升来自 Smooth-On 的[simact 聚氨酯橡胶填充。橡胶固化后，他将它们从模具中取出，粘在木块上。最终的结果看起来和你从工艺品商店买到的一样好。](https://www.smooth-on.com/product-line/simpact-series/)

这里使用的过程与我们最近报道过的 3D 打印饼干模具非常相似，尽管我们不得不假设这些小块饼干并不好吃。当然，[如果你有一台小型数控机床](https://hackaday.com/2014/02/12/cheap-resourceful-diy-mini-cnc-routermill-contraption/)，你可以直接从橡胶上切下印记，完全跳过模具步骤。