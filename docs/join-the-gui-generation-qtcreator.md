# 加入 GUI 一代:QTCreator

> 原文：<https://hackaday.com/2016/07/08/join-the-gui-generation-qtcreator/>

如今，越来越多的项目需要软件组件。随着一切都被联网，避免为桌面或电话环境提供软件以及嵌入式设备中的代码变得越来越难。

如果你做过很多嵌入式系统的工作，你可能已经知道 C 和 C++。如果是这样的话，很容易找到一个 C 编译器，并编写一个命令行应用程序来做你想做的事情。问题是今天的用户对命令行有不同程度的恐惧，从不舒服到纯粹的恐惧。在移动设备上，他们可能甚至不知道如何使用命令行。我已经等待 WIMP(窗口/图标/鼠标/指针)时尚消失多年了，但即使是我也不得不承认，它可能会在可预见的未来出现。

[![qtrigol](img/108cf4932d6294da6e51aae4ea285734.png)](https://hackaday.com/wp-content/uploads/2016/06/qtrigol.png) 那么有什么选择呢？其实也不少。但是，我想说的是一个免费的、部署选项广泛的、使用 C++、容易上手的:Qt。具体来说，用 QtCreator 创建程序(见右图)。是的，还有其他的选择，你可以用多种方式开发 Qt 程序。

你可能会觉得 Qt 不是免费的。曾经有一段时间，它对开源项目是免费的，但对商业项目是免费的。然而，最近的许可变化(从版本 4.5 开始)使得它更像是使用 gcc。您可以选择使用 LGPL，这意味着在封闭软件中使用 Qt 共享库很容易。你也可能认为许多奇怪的结构以不寻常的方式“扩展”了 C++。事实是，确实如此，但是有了 QtCreator，你可能不需要知道任何这方面的东西，因为这个工具会为你设置大部分，如果不是全部的话。

## 背景

如果你曾经使用过 Visual Basic 或类似的东西，你会觉得 QtCreator 很好用。您可以在表单上放置按钮、文本编辑框和其他小部件，然后用代码备份它们。当你按下按钮时，按钮会产生信号。有许多信号，如文本改变或小部件(控件)被创建或破坏。

为了处理信号，对象提供了一个插槽。有一个元编译器可以预处理你的 C++代码，把所有的信号和槽转换成普通的 C++。好消息是:你并不真的在乎。在 QtCreator 中，您可以编写代码来处理按钮的按下，具体是如何发生的并不太令人担心。

QtCreator 有针对不同平台的工具包，一般来说，代码可以在平台之间合理地移植。如果你确实想为 Android 或 iOS 做移动开发，那么在开始之前一定要了解这些限制，这样你就可以避免将来的陷阱。

## 你需要上课

像许多类似的框架一样，Qt 使用一个应用程序类(QtApplication)来表示一个无所事事的应用程序。你的工作是定制一个子类，并让它做你想要的。你可以添加小工具，如果你喜欢，你甚至可以添加更多的屏幕。您可以将信号连接到现有插槽或新插槽。

有很多类可用，在线文档也相当不错。根据您使用的 Qt 版本，您需要找到正确的页面(或者让 QtCreator 帮您找到)。然而，为了吊起你的胃口，[这里是 Qt5 参考页](https://doc.qt.io/qt-5/reference-overview.html)。在那里，您可以找到 GUI 部件、字符串、网络套接字、数据库查询甚至串行端口的类。

我可以做一个完整的使用 QtCreator 的教程，但是这是一个重复的工作。已经有一个很好的[开始一个](https://wiki.qt.io/Basic_Qt_Programming_Tutorial)提供。你会发现有大量的文档。

## 轻便

如何枚举串口？要看平台吧？在 Qt 中，特定于平台的部分对您是隐藏的。例如，下面的一段代码填充了一个带有可用串行端口的组合框:

```
MainWindow::MainWindow(QWidget *parent) :
 QMainWindow(parent),
 ui(new Ui::MainWindow)
{
 ui->setupUi(this);
// initialize list of serial ports
 ports = QSerialPortInfo::availablePorts();
// fill in combo box
 for (int i=0; i<ports.length(); i++) 
 {
   ui->comport->addItem(ports[i].portName(), QVariant(i));
 }
}

```

对象提供了一个串口对象数组。`ui->comport`是一个组合框，`addItem`方法让我为每个选择输入一个显示字符串和一个数据项。在这种情况下，显示的是端口的`portName`，额外的数据只是数组中的索引(作为一种变体，可以是不同类型的数据，而不仅仅是数字)。当您选择一个端口时，索引让程序查找端口，例如，打开它。

当组合框改变时，会出现一个`currentIndexChanged`信号。这是插槽处理程序:

```
void MainWindow::on_comport_currentIndexChanged(int index)
{
 QString out;
 // get selected index
 int sel=ui->comport->currentData().toInt();
// build up HTML info string in out
 out="<h1>Serial Port Info</h1>";
 ui->output->clear();
 out += ports[sel].portName() + " " + ports[sel].description() + "
";
 out += ports[sel].systemLocation() + "
";
 if (ports[sel].hasVendorIdentifier() && ports[sel].hasProductIdentifier())
 out += ports[sel].manufacturer() + " ("+ QString::number(ports[sel].vendorIdentifier(),16) + ":" + QString::number(ports[sel].productIdentifier(),16) + ")";
 // and put it on the screen
 ui->output->setText(out);
}
```

在这种情况下，结果是关于串行端口的信息。您可以在下面看到结果输出。`QString`是 Qt 的字符串类，显然，文本显示小部件理解一些 HTML。

[![qtserial](img/9ff3c4b85e8de415bf8f10086b8259e7.png)](https://hackaday.com/wp-content/uploads/2016/06/qtserial.png)

## 不仅仅是图形用户界面

您可以使用 Qt 开发控制台应用程序，但是许多提供的类没有意义。甚至还有一个用于嵌入式的 [Qt(本质上是没有 GUI 的 Linux)。你可以找到](https://wiki.qt.io/Qt_for_Embedded_Linux)[树莓皮](https://wiki.qt.io/RaspberryPi_Beginners_Guide)和[猎兔犬皮](https://wiki.qt.io/Qt_on_the_BeagleBoard)的指南。

在移动端，你可以瞄准[安卓](https://doc.qt.io/qt-5/androidgs.html)、 [iOS](https://doc.qt.io/qt-5/examples-ios.html) ，甚至黑莓，以及其他。像任何事情一样，它可能不仅仅是“按下一个按钮”，一个移植的应用程序就会掉出来了。但与从头开始重新编写移动应用程序相比，它仍然可以减少开发时间和成本。

## 获胜者是…

我敢肯定，如果你想要一些替代方案，我们的评论区将充满建议。有些可能是好的。但令我吃惊的是，并不是每个人都有相同的需求和背景。对你来说最好的工具可能不适合我。我发现 Qt 很有用，也很高效。

即使 Qt 不是你的首选工具，它仍然可以方便地放在你的工具包里。你永远不知道什么时候会需要一个又快又脏的跨平台应用。