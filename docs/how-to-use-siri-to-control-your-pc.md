# Siri 通过 Python 和 Gmail 控制你的 PC

> 原文：<https://hackaday.com/2017/04/27/how-to-use-siri-to-control-your-pc/>

如今，语音助手在设备上变得越来越普遍。众所周知，Siri 特别擅长回应自然语言和尖刻的回应。相比之下，谷歌助手只能执行最明显的命令，这位作者甚至不确定微软的 Cortana 是否能理解英语。因此，如果你想对你的电脑进行语音控制，选择 Siri 作为你的首选武器是有意义的。[[sanj eet]在此提供帮助，让 Siri 能够通过 Python 控制电脑。](https://thereallycoolstuff.wordpress.com/2017/02/26/using-siri-to-control-your-computer/)

第一步是将 iPhone 的 Notes 应用程序连接到 Gmail 帐户。[Sanjeet]建议出于安全原因使用单独的帐户，因为您需要将用户名和密码放在 Python 脚本中。Python 脚本每秒都会检查 Gmail 帐户，从 iPhone 中寻找新的笔记。然后，它就像告诉 Siri 做一个笔记一样简单(例如，“Siri，笔记关机”)，Python 脚本就可以拾取该命令，并相应地采取行动。

这是让 Siri 执行您的命令的一种快速而简单的方法。还有其他奇特的方法可以做到这一点，比如在你的家庭网络中捕捉 Siri 的 WiFi 数据。