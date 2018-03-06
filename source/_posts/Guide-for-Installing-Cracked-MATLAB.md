---
title: 破解版MATLAB安装教程
categories:
  - IT
tags:
  - zh-CN
date: 2018-03-05 23:44:13
icon: download
---
> 先简略写个大概教程，后期再修缮措辞。

## 下载及解压
目前最新版本的MATLAB是R2017b，可以通过磁力链进行**[[下载]](magnet:?xt=urn:btih:1b2aaaa47a15bd8ca24844093547da2327b21af7&dn=MATLAB%20R2017b%20%5bPC%5d%20%5bx64%5d.zip&tr=udp%3a%2f%2ftracker.leechers-paradise.org%3a6969&tr=udp%3a%2f%2fzer0day.ch%3a1337&tr=udp%3a%2f%2fopen.demonii.com%3a1337&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969&tr=udp%3a%2f%2fexodus.desync.com%3a6969)**：

```
magnet:?xt=urn:btih:1b2aaaa47a15bd8ca24844093547da2327b21af7&dn=MATLAB%20R2017b%20%5bPC%5d%20%5bx64%5d.zip&tr=udp%3a%2f%2ftracker.leechers-paradise.org%3a6969&tr=udp%3a%2f%2fzer0day.ch%3a1337&tr=udp%3a%2f%2fopen.demonii.com%3a1337&tr=udp%3a%2f%2ftracker.coppersurfer.tk%3a6969&tr=udp%3a%2f%2fexodus.desync.com%3a6969
```

如果电脑有迅雷之类的下载器的话，点击下载链接便能自动跳出下载界面了，或者也可以新建下载任务，把磁力链粘贴进去下载。下载后是个压缩包，大小为11.2GB，占空间较大，请事先确保有足够的硬盘空间。下载后进行解压，解压后的文件目录如下图所示。

![](https://i.loli.net/2018/03/06/5a9d6c45951dc.png)

## 安装及破解
然后双击Setup.exe进行安装。

![](https://i.loli.net/2018/03/06/5a9d6c459c301.png)

选择第二个选项以使用安装密钥。

![](https://i.loli.net/2018/03/06/5a9d6c459cd9f.png)

然后填入密钥：
```
09806-07443-53955-64350-21751-41297
```

![](https://i.loli.net/2018/03/06/5a9d6c459b579.png)

然后这个是选择安装目录，默认是C盘，我个人习惯是装在D盘，你们随意，但要确保有足够的空间，保险起见留个至少15GB的空间吧。

点下一步后会让你选择安装什么组件，如果你硬盘空间够大的话，可以保持默认的全选。不想全选的话就只选那个MATLAB 9.3吧，只选那个的话就只会占用2GB多的空间，不过也会少一些功能，具体少什么功能我暂时没测试过，反正我暂时能用就是了。

再点击下一步后就是安装完成了。然后打开安装好的MATLAB，它会提示激活。

![](https://i.loli.net/2018/03/06/5a9d6c46011eb.png)

选第二个选项，然后点下一步，然后就选择激活证书的目录。激活证书在一开始你下载后解压的那个文件夹里。点击`Browse...`，找到之前那个文件夹里面的`- crack & instructions -`文件夹，选择`license_standalone.lic`这个文件。如图所示。

![](https://i.loli.net/2018/03/06/5a9d6c46dc982.png)

然后点下一步就会提示激活成功了。

## 重要的最后一步

虽然提示激活成功，**但你还需要做下面这一步**。

找到一开始下载后解压的那个文件夹，然后`- crack & instructions -`→`R2017b`→`bin`→`win64`，找到`netapi32.dll`这个文件，把它复制粘贴到软件的安装目录下。如果你之前按照默认目录的话，那么它就位于
```
C:\Program Files\MATLAB\R2017b\bin\win64
```

把那个文件粘贴进去。如图所示。

![](https://i.loli.net/2018/03/06/5a9d6c4596f28.png)

![](https://i.loli.net/2018/03/06/5a9d6c46d9eda.png)

## 完成
嗯，这样基本上就完成了，再次打开MATLAB应该就可以用了，至少在我的电脑上是亲测成功的。本教程仅适用于从我给出的那个磁力链所下载的MATLAB，其他地方下载的往往不适用。不过从其他地方下载的，里面一般也会有说明的，按照说明做估计也能成功。