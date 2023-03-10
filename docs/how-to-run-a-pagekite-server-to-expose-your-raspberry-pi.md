# 如何运行 Pagekite 服务器来展示您的树莓 Pi

> 原文：<https://hackaday.com/2016/09/21/how-to-run-a-pagekite-server-to-expose-your-raspberry-pi/>

上次我向您展示了如何通过使用 Pagekite 的反向代理在 Raspberry Pi(或者实际上，任何类型的设备)上公开 web 服务。在您的 Pi 上，您只需要一个简单的 Python 脚本。然而，它也依赖于 Pagekite 服务器，这并不总是方便的。免费服务是有限度的，你不能控制整个事情。好消息是双重的:用于设置客户端的 Python 脚本也可以设置服务器。另一个好消息是整个系统都是开源的。

实际上，如果你有一台一直开着的电脑，并且有一个可以在公共互联网上找到的 IP 地址，你就可以运行你自己的 Pagekite 服务器(他们称之为前端),为你自己的后端服务。

## 初始设置

正如我提到的，你需要一台能上网的电脑。嗯，从技术上来说，一台对你希望使用的所有客户端都可见的计算机，包括后端。它需要一些工具，包括 Python，但没有什么特别的。你还需要控制你的 DNS——具体怎么做取决于你的服务器是如何设置的。在我的例子中，我在数据中心的机架上有一台服务器，所以我有自己的 DNS 服务器(名为)。

Pagekite 网站有 RPM 和 deb 包的安装包。我建议您从在服务器上安装开始，使用与您的打包系统相匹配的方法。这将放入一个名为/etc/pagekite.d 的新目录，并安装一个启动脚本(/etc/init.d/pagekite)。

但是，默认设置是退出，不启动任何东西。更重要的是，示例文件被设置为好像计算机想要与提供的 Pagekite 前端对话(pagekite.me)。如果你想经营自己的公司，你必须做出一些改变。

## 裸体派对

如果你在互联网上有一台服务器，有一些方法可以将域名(如 hackaday.com)输入 DNS 系统，指向一个特定的 IP 地址。在我的情况下，我拥有域名 hotsolder.com，所以我决定让 dyn.hotsolder.com 成为我的 Pagekite 前端。我也希望能够创建像 3dprinter.dyn.hotsolder.com 子域名。

为此，我需要对我的 DNS 进行一些配置更改:

```
dyn           IN        A 173.201.49.198 
*.dyn         IN        A 173.201.49.198

```

很明显，我的 IP 地址就是显示的那个。所有的名字都是相对于 hotsolder.com 的，所以没有必要在那两行中指定。如果你的托管公司处理你的 DNS，你必须决定如何做类似的改变。或者你可以告诉他们你需要两个 A 记录，他们应该知道这意味着什么。结果是你的主机名(dyn.hotsolder.com 或 anything.dyn.hotsolder.com)进入你的服务器(下图中的 Pagekite 服务器)。

[![](img/bf632bbae009b4d218924917bdab7452.png)](https://hackaday.com/wp-content/uploads/2016/09/networkdiagram2-e14735283292891.png)

## 主机设置

Pagekite 包会在/etc/pagekite.d 中留下两个重要文件:10_account.rc 和 20_frontends.rc，第一个文件是为什么服务不会启动。事实是，对于使用脚本作为前端，你根本不需要这个文件。为了以防万一，我注释掉了所有的行，但是你也可以删除它。阻止它启动的行是这样的:

```
abort_not_configured
```

其他线路设置您到 pagekite.me 服务器的连接。我们不打算这样做，所以你可以删除这些行或整个文件。

20_frontends.rc 文件应该连接到远程前端。在这种情况下，我们希望成为前端，所以我在这里输入了以下内容:

```
isfrontend
ports=8080,80,443,2222
rawports=virtual
protos=http,https,raw
domain=http,https,http-8080,raw-2222:*.dyn.hotsolder.com:$$$SECRET$$$
domain=http,https,http-8080,raw-2222:dyn.hotsolder.com:$$$SECRET$$$
```

您还可以设置一个证书文件并指向它，但是如果您想这样做，您可以[阅读文档](https://pagekite.net/wiki/Floss/TechnicalManual/#tls)(查找–TL _ default 和–TLS _ endpoint 选项以及–Fe _ certname 和–ca _ certs)。事实上，在同一文档中，您可以了解所有选项，如 isfrontend 和 ports。

## 客户端设置

默认情况下，Pagekite 脚本在~/.pagekite.rc 中查找设置。如果您计划使用 Pagekite 服务器，您最好不要去管这个文件，而是创建一个新的配置。您可以在 Pi 或其他客户端计算机上安装相同的包—记住，在前端(面向互联网的计算机)和后端(运行服务器的计算机)上使用相同的脚本。

如果您想从命令行运行，请考虑使用:

```
pagekite --clean --optfile=/home/YOURUSERID/.pagekite.CUSTOM.rc
```

显然，您需要替换您的 USERID 和 CUSTOM 来适应您的目的。如果你正在使用一个包，并且让 Pagekite 自动启动，你需要查看/etc/pagekite.d，在 20_frontends.rc 中你可以配置你想要与之对话的每一个前端服务器。

这是我档案的一部分:

```
webpath = dyn.hotsolder.com/8080:/:default:/tmp/httpd
webpath = dyn.hotsolder.com/80:/:default:/home/alw/Photos
frontend=dyn.hotsolder.com:443
service_on=http:dyn.hotsolder.com:localhost:builtin:@kitesecret
service_cfg=dyn.hotsolder.com/80:indexes:True
service_on=raw-2222:dyn.hotsolder.com:localhost:22:@kitesecret
```

@kitesecret 引用了更上面的一行(或在 10_accounts 文件中):

```
kitesecret=$$$SECRET$$$
```

当然，这必须与前端的设置相匹配。

## 有趣的事情

对于 http 请求，一切都如您所料。service_on 和 service_cfg 行设置了内置的 Web 服务器(您不必使用它),文档中说这些是可以更改的。否则，设置事情是相当简单的。

当您想做一个原始端口时，问题就出现了。在我的例子中，我想向外界公开端口 22 上的 ssh 服务器。当然，我的公共计算机在那个端口上已经有一个 ssh 服务器了。那没问题。Pagekite 可以将端口 2222 上的传入流量转换到后端的端口 22。算是吧。

原始端口实际上通过 http 端口。例如，要使 ssh 工作，您需要使用 netcat 从端口 443 进行代理。细节在[文档](https://pagekite.net/wiki/Howto/SshOverPageKite/)中，但简而言之就是你需要在~/中进行如下配置。ssh/config:

```
Host dyn.hotsolder.com
   CheckHostIP no
   ProxyCommand /bin/nc -X connect -x %h:443 %h %p
```

## 少年派的互联网

如果你控制你连接的每一个网络，这可能就没什么意思了。如果你不介意在两边设置 VPN，你也不需要这种东西。然而，如果您需要在防火墙后甚至在动态 IP 地址上部署解决方案，您可能会发现反向代理方法正是您所需要的。

当然，总有其他方法可以解决问题。例如，您可以使用动态 IP 提供程序来处理动态 IP。然而，通过未知防火墙的隧道有点困难。