---
title: Hello World! — How I Built This Blog
date: 2017-07-27 12:22:09
icon: fa-github
tags:
- en
- Git
- Hexo
categories:
- IT
---
> Hello World!

This is the first article written by me on this blog. I will show you how I built the blog. It took me several days to practice using Hexo and [GitHub Pages](https://pages.github.com/). It is not a easy job for me since I know little about programming. But I will share what I have done step by step with you if you are a greenhand like me and that may help you a little. At the beginning, there are two blog software for me to choose, [Jekyll](https://jekyllrb.com/) and [Hexo](https://hexo.io/). Finally, I decided to adopt Hexo.

## Preparation
Hexo requires [Git](https://git-scm.com/) and [Node.js](https://nodejs.org/en/). For Git, I installed GitHub for Windows. Then use Git Shell to install Hexo. By the way, my OS is MS Windows 8.1. GitHub for Windows will creat a folder named `GitHub` in your default `Documents` folder automatically. What you should do first is to launch Git Shell. You will see these:
```shell
Windows PowerShell
Copyright (C) 2014 Microsoft Corporation. All rights reserved.

~\Documents\GitHub>
```
Just type `npm install hexo-cli -g` then press Enter. Wait for the installing of Hexo. Meanwwhile I created the repository named `dqwyy.github.io` on GitHub. After the installing of Hexo, I initialised Hexo in `%USERPROFILE%\Documents\GitHub\dqwyy.github.io\` by typing (exclude the `$` symbol, the same below)
```shell
$ hexo init %USERPROFILE%\Documents\GitHub\dqwyy.github.io\
$ cd %USERPROFILE%\Documents\GitHub\dqwyy.github.io\
$ npm install
```

## Beautify
I don't like the default theme landscape so I was looking for themes. Finally I found [anodyne](https://github.com/klugjo/hexo-theme-anodyne), the present theme of my blog. I installed it by typing
```shell
$ git clone https://github.com/klugjo/hexo-theme-anodyne themes/anodyne
```
then delete the hidden `.git` floder. To customize the theme, I modified `%USERPROFILE%\Documents\GitHub\dqwyy.github.io\themes\anodyne\_config.yml`.

## Upload Codes
Before uploading the codes to GitHub, I used GitHub for Windows to link the local repository to remote repository, which would generate a hidden `.git` floder. It is of great importance to put the codes in a branch other than `master`, as for me, it's `hexo`. Everytime I change files in local repository, I type these command under the `hexo` branch: (words behind `#` are comment)
```shell
$ git checkout hexo    # Switch to branch hexo.
$ git add --all    # preparation for commit.
$ git commit -m "message"
$ git push origin hexo    # ATTENTION: "hexo" here, not "master".
```

## Deploy
Deploying is going to have the blog shown on <https://dqwyy.github.io>, or the blog is shown on <http://localhost:4000> only. Firstly, modify `%USERPROFILE%\Documents\GitHub\dqwyy.github.io\_config.yml`.
```yml
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: https://github.com/dqwyy/dqwyy.github.io.git
  branch: master
```
Then type these on the Git Shell:
```shell
$ npm install hexo-deployer-git --save    # it's only neccessary at the first time.
$ hexo genarate    # or abbreviate to "hexo g"
$ hexo deploy    # or abbreviate to "hexo d"
```
DONE!

## To Do
I am going to install more useful [plugins](https://hexo.io/plugins/) in the future.

Well, once again:
> Hello, <del>Sekai</del> World!

![](http://image.wangchao.net.cn/baike/1267577209651.jpg "It is all Sekai's fault, not mine!")

## References
[1] 阮一峰. [Git远程操作详解](http://www.ruanyifeng.com/blog/2014/06/git_remote.html). 阮一峰的网络日志. 2014-06-12. <small>(zh-CN)</small><br>
[2] [Hexo Documentation](https://hexo.io/docs/). Hexo.<br>
[3] Mu Bit. [How to set up Free Blog using Hexo JS on Github](https://youtu.be/tEFKJeAtGqk?list=PL4IWl8w32SvV5p3TIXEDYUkH9ACtxkBdT). YouTube. 2016-10-01. <small>(en)</small><br>
[4] 令狐葱. [手把手教你使用Hexo + Github Pages搭建个人独立博客](https://linghucong.js.org/2016/04/15/2016-04-15-hexo-github-pages-blog/). 令狐葱@前端笔记. 2016-04-15. <small>(zh-CN)</small>