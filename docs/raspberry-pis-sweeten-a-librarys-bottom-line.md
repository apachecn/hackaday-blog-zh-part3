# 树莓汁增加了图书馆利润

> 原文：<https://hackaday.com/2016/05/16/raspberry-pis-sweeten-a-librarys-bottom-line/>

这是 Pi 的一个很好的真实使用案例——小型计算机的一个小任务。[维京–]在公共图书馆工作。像许多公共图书馆一样，这个图书馆有目录专用的终端，与你预定用来获取猫视频和宝石迷阵的电脑是分开的。[目录计算机需要升级，【维京—】用 raspi](https://www.reddit.com/r/raspberry_pi/comments/4ivnse/i_work_at_a_public_library_and_replace_all_our/)把它们都换掉了。

他们每次都运行 Raspbian 并以干净的配置文件直接启动到 Chromium。否则 pi 将被完全锁定，只能通过 SSH 访问。专用 WiFi 网络和白名单网络访问有助于确保他们的安全。Pis 在五分钟不活动后重新启动，这将删除所有登录凭证和书签。

这些终端分散在图书馆各处。最靠近前台的人将他们的 Pi 安装在显示器背面的 VESA 底座上。其他的都锁在柜子里，这样就不会被顾客偷了。图书馆的预算已经够少了。[Viking–]能够通过构建一个原型来展示系统的简单性和预计的成本节约，从而获得管理层对项目的认可。多亏了几个 cron jobs，Pis 每天晚上都关闭监视器，每年节省数百美元。