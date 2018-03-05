---
title: IRC使用教程
categories:
  - IT
tags:
  - zh-CN
date: 2017-08-06 00:13:35
icon: fa-hashtag 
---
目录
<!-- toc -->
----
IRC，英文全称是[Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat)，是一种比较传统的即时聊天方式。本文将介绍IRC的一些使用方法，论述对象以[Freenode](https://en.wikipedia.org/wiki/Freenode)网络为主，[Rizon](https://www.rizon.net)为辅，因此极少数论述可能不适用于其他的IRC网络，但大多数论述还是通用的。

## 客户端
要访问IRC网络，您需要一个IRC客户端。在不同的平台上，IRC有不同的客户端。如果您只是偶尔使用IRC的话，那么可以使用网页版的IRC客户端。网页版的IRC客户端优点在于不必特地去下载安装客户端软件，而是直接在浏览器上便可以使用IRC。其缺点就是连接不是很稳定且功能较少。对于Freenode网络，可以使用由[qwebirc](http://www.qwebirc.org/)开发的[这个网页版客户端](https://webchat.freenode.net/)；对于Rizon网络，则可以使用由同一个团队开发的[这个网页版客户端](https://www.rizon.net/chat)。这些网页版客户端依赖于JavaScript。

如果您跟在下一样是IRC的长期高频使用者，那么在下推荐您使用更加好用的IRC客户端而不是网页版客户端。如果您像在下一样使用开源免费的Firefox浏览器，那么您可以下载[ChatZilla](http://chatzilla.hacksrus.com/)这个客户端来使用，在下目前正在使用这个客户端。这个客户端是以浏览器插件的形式存在的。

至于安卓平台上，我使用的是[AndroIRC](http://www.androirc.com/)。这个客户端虽然不是很完善，不过是我用得最顺手的一个了。安卓平台上其他的客户端难以使我满意。AndroIRC的UI语言无法自己选择，估计是自动匹配系统语言。其中的简体中文翻译质量不是很好。在使用上，自动登录存在着Bug，解决方法是可以通过自动指令功能来进行认证。

如果您没有使用Firefox，且您在使用Windows系统的话，那么您可以试试[mIRC](http://www.mirc.com/index.html)。如果您使用的是其他系统的话，请根据您的操作系统选择客户端，详情可参见英文维基百科[对于不同平台的IRC客户端的比较](https://en.wikipedia.org/wiki/Comparison_of_Internet_Relay_Chat_clients)条目。

大多数客户端都已经自动配置了一些IRC网络的连接，一般都能够直接选择您要进入的IRC网络，Freenode一般是包括在内的。但是偶尔会遇到一些需要自己配置的情况，或者是您想连接一些比较冷门的IRC网络，那么就应该自己配置。配置一般掌握两个点就行了，第一个是IRC网络的网址，例如Freenode是`irc.freenode.net`或`chat.freenode.net`，Rizon是`irc.rizon.net`；第二个是IRC网络的连接端口，不同IRC网络的连接端口不同，而且启用[SSL](https://zh.wikipedia.org/wiki/%E5%82%B3%E8%BC%B8%E5%B1%A4%E5%AE%89%E5%85%A8%E6%80%A7%E5%8D%94%E5%AE%9A)的端口和不启用SSL的端口也不同，具体可以参照各IRC网络的官方网站上的说明。例如Freenode的明文连接端口是`6697`和`7000`，SSL加密连接端口是`7070` <sup>[[Ref]](https://freenode.net/kb/answer/chat)</sup>；Rizon的明文连接端口是`6660`-`6670`和`7000`，SSL加密连接端口是`6697`和`9999` <sup>[[Ref]](https://www.rizon.net/info/access)</sup>。

## IRC的聊天环境
IRC的聊天环境主要以频道为主，而个人私聊（Private Message, PM）仅是一个附加功能。在IRC上，会有不同的IRC网络，例如本文主要介绍的Freenode，还有有很多日本动漫相关频道的Rizon等。不同的IRC网络之间无法相通，例如Freenode上有个`#anime`频道，Rizon上面也有一个`#anime`频道，但是两者的聊天记录并不相通，可以把他们看成是两个完全不同的频道。

IRC的频道名以`#`开头，例如在Freenode上，有`#wikipedia-zh`、`#anime`等频道，每个频道都有自己的聊天主题，要加入频道，可以在连接好Freenode后在输入框输入`/join #channel`来进入频道，如果您忘了加上`#`号，很多客户端都是支持不加`#`自动补全的，因此往往也能进入到相应的频道。而在Freenode上，还有一些以两个井号开头的频道，如`##c++`频道。据Freenode[关于频道名称的官方指南](https://freenode.net/kb/answer/namespaces)，这种以两个井号开头的频道是非官方频道。但据我个人理解，其实或许没有这么严格，Freenode这么要求主要是想告诉用户们，如果你们想要建立某个频道，但你们不是官方的频道，那么应该用两个井号开头的。但往往官方不会很在意这个频道，例如你们是某部动漫的粉丝，我们以[Key社](https://zh.wikipedia.org/wiki/Key_(%E9%81%8A%E6%88%B2%E5%93%81%E7%89%8C%29)制作的游戏《[Rewrite](https://zh.wikipedia.org/wiki/Rewrite)》为例好了，因为这也是在下最喜欢的游戏。作为《Rewrite》的粉丝，在下不是Key社的工作人员，因此在下是非官方，那么按照Freenode的说明在下应该建立一个`##Rewrite`频道，而不是`#Rewrite`频道。前者由粉丝建立，后者由官方建立。然而就目前这个趋势，Key社应该是不会来Freenode IRC建立频道的，因此这时候我建立一个`#Rewrite`频道也无大碍。但是假如以后有一天Key社真的要来Freenode IRC建立频道了，那么根据Freenode的使用条款，他们便可以依[使用条款](https://freenode.net/policies)回收我对频道的管理权。此外，从技术上讲，你也可以建立大于两个井号开头的频道，如`###Rewrite`、`####Rewrite`、`#####Rewrite`等等。但最常用的还是以一个井号开头。

