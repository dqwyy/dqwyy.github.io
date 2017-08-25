---
title: IRC使用教程
categories:
  - IT
tags:
  - zh-CN
  - IRC
  - IM
date: 2017-08-06 00:13:35
icon: fa-hashtag 
---
目录
<!-- toc -->
----
IRC，英文全称是[Internet Relay Chat](https://en.wikipedia.org/wiki/Internet_Relay_Chat)，是一种比较传统的即时聊天方式。本文将介绍IRC的一些使用方法，主要以[Freenode](https://en.wikipedia.org/wiki/Freenode)网络为例，因此个别论述可能不适用于其他的IRC网络。

## 客户端
要访问IRC网络，您需要一个IRC客户端。在不同的平台上，IRC有不同的客户端。如果您只是偶尔使用IRC的话，那么可以使用网页版的IRC客户端。网页版的IRC客户端优点在于不必特地去下载安装客户端软件，而是直接在浏览器上便可以使用IRC。其缺点就是连接不是很稳定且功能较少。对于Freenode网络，可以使用由[qwebirc](http://www.qwebirc.org/)开发的[这个网页版客户端](https://webchat.freenode.net/)；对于Rizon网络，则可以使用由同一个团队开发的[这个网页版客户端](https://www.rizon.net/chat)。这些网页版客户端依赖于JavaScript。

如果您跟在下一样是IRC的长期高频使用者，那么在下推荐您使用更加好用的IRC客户端而不是网页版客户端。如果您像在下一样使用开源免费的Firefox浏览器，那么您可以下载[ChatZilla](http://chatzilla.hacksrus.com/)这个客户端来使用，在下目前正在使用这个客户端。这个客户端是以浏览器插件的形式存在的。

至于安卓平台上，我使用的是[AndroIRC](http://www.androirc.com/)。这个客户端虽然不是很完善，不过是我用得最顺手的一个了。安卓平台上其他的客户端难以使我满意。AndroIRC的UI语言无法自己选择，估计是自动匹配系统语言。其中的简体中文翻译质量不是很好。在使用上，自动登录存在着Bug，解决方法是可以通过自动指令功能来进行认证。

如果您没有使用Firefox，且您在使用Windows系统的话，那么您可以试试[mIRC](http://www.mirc.com/index.html)。如果您使用的是其他系统的话，请根据您的操作系统选择客户端，详情可参见英文维基百科[对于不同平台的IRC客户端的比较](https://en.wikipedia.org/wiki/Comparison_of_Internet_Relay_Chat_clients)条目。

## IRC的聊天环境
IRC的聊天环境主要以频道为主，而个人私聊（Private Message, PM）仅是一个附加功能。在IRC上，会有不同的IRC网络，例如本文主要介绍的Freenode，还有与日本动漫相关的Rizon等。不同的IRC网络之间无法相通，例如Freenode上有个`#anime`频道，Rizon上面也有一个`#anime`频道，但是两者的聊天记录并不相通，可以把他们看成是两个完全不同的频道。

IRC的频道名以`#`开头，例如在Freenode上，有`#wikipedia-zh`、`#anime`等频道，每个频道都有自己的聊天主题，要加入频道，可以在连接好Freenode后在输入框输入`/join #channel`来进入频道，如果您忘了加上`#`号，很多客户端都是支持不加`#`的，因此往往也能进入到相应的频道。