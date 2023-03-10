# 选项出血-阿帕奇出血在不常见的配置

> 原文：<https://hackaday.com/2017/09/19/optionsbleed-apache-bleeds-in-uncommon-configuration/>

【Hanno bck】最近[在 Apache webserver 中发现了一个漏洞，](https://blog.fuzzing-project.org/60-Optionsbleed-HTTP-OPTIONS-method-can-leak-Apaches-server-memory.html)影响 Apache HTTP Server 2.2.x 到 2.2.34 和 2.4.x 到 2.4.27。这个 bug 只影响在`.htaccess`文件中有特定配置的 Apache 服务器。该漏洞被称为 Optionsbleed，是 Apache HTTP 中的释放错误后使用，导致 web 服务器在响应 HTTP OPTIONS 请求时回复损坏的 Allow 标头。这可能会从服务器进程中泄漏可能包含敏感信息的任意内存片段。内存块在多次请求后会发生变化，因此对于易受攻击的主机来说，任意数量的内存块都会泄漏。

与过去著名的 Heartbleed 错误不同，Optionsbleed 只泄漏一小部分内存，更重要的是，默认情况下只影响一小部分主机。然而，允许`.htaccess`文件改变的共享托管环境对它非常敏感，因为来自一个用户的流氓`.htaccess`文件可能会泄漏整个服务器的信息。扫描 Alexa 前 100 万发现 466 主机与腐败的 Allow 头，所以它似乎影响不是很大。

如果网站管理员试图将“Limit”指令与无效的 HTTP 方法一起使用，就会出现该错误。我们决定用这样一个简单的`.htaccess`文件来测试这种行为:

```
<Limit A>
 Allow from all
 </Limit>
 <Limit BB>
 Allow from all
 </Limit>
 <Limit CCC>
 Allow from all
 </Limit>
```

很快，在十几个请求之后，网络服务器的回复明显开始变得非常可疑:

```
$ curl -sI -X OPTIONS http://10.9.0.1/index.html

HTTP/1.1 200 OK
 Date: Tue, 19 Sep 2017 15:03:59 GMT
 Server: Apache/2.4.7
 Allow: GET,HEAD,,allow,HEAD,,allow,HEAD,POST,OPTIONS,8���,HEAD,8����,HEAD,dex.html,HEAD, ���,HEAD, ����,HEAD,all,HEAD,,HEAD
 Content-Length: 0
 Content-Type: text/html
```

Apache web 服务器用户应该检查现有的配置文件并进行更新。大多数发行版现在或者很快就应该有更新包了。Apache 2.2 版的补丁可以在这里找到，Apache 2.2 版的补丁可以在这里找到。共享主机环境的 web 服务器管理员应该尝试尽快更新，因为在这些情况下，更大的风险是一个用户可能会影响其他所有人。