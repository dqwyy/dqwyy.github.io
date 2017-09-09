---
title: GFW Circumvention
categories:
  - IT
tags:
  - en
  - VPN
  - GFW
date: 2017-08-04 17:02:16
icon: fa-internet-explorer 
---
Some websites like Google, Facebook, Twitter and so on are not accessable in Mainland China due to the GFW ([Great Firewall of China](https://en.wikipedia.org/wiki/Great_Firewall)\). I am going to record some methods to circumvent the GFW here, which are what I recommend.

## Modify Your hosts Files
The computer file [hosts](https://en.wikipedia.org/wiki/Hosts_%28file%29) is an operating system file that maps hostnames to IP addresses, whoes location is `%SystemRoot%\System32\drivers\etc\hosts` in Windows. DNS cache pollution, which is one of the GFW's tricks, could be circumvented by modifying the hosts files. However, GFW is dynamic, so hosts should be updated in time. Here are two related repos on GitHub. This method is totally free. But it doesn't work for every GFWed websites or all time.

* <s><https://github.com/racaljk/hosts>, IPv4 hosts.</s> (This repo had stopped updating.)
* <https://github.com/googlehosts/hosts> Telegram Group: [@googlehosts](https://t.me/googlehosts)
* <https://github.com/sy618/hosts>
* <https://github.com/lennylxx/ipv6-hosts>, IPv6 hosts, supports YouTube.

## Lantern
Lantern is a [VPN](https://en.wikipedia.org/wiki/Virtual_private_network) software. But it is not recommended for long-term-use because it only provides 500MB per month for free. I only use it temporarily.

Lantern in GitHub: <https://github.com/getlantern/lantern>

## Shadowsocks
Shadowsocks is my favourate software. Accounts are neccessary. GitHub Link: <https://github.com/shadowsocks/shadowsocks-windows>

### Free Accounts
* [iShadow](http://ss.ishadowx.com/index.html)
Alternate URL: <http://isx.yt/> & <http://isx.tn/>
Send any text email to the following address to get the latest link: <admin@ishadowsocks.com>
iShadow provides 9 free accounts for shadowsocks. All servers will be reset and change its password in 00:00, 6:00 and 12:00 (UTC+8) everyday. For example, a Japan server is shown below as a QR Code.
![Sorry, the picture doesn't measure to load because of GFW, please use a VPN first.](http://ss.ishadowx.com/img/qr/jpa.png "Japan-Linode1 Server, please scan this QR Code with your Shadowsocks client")

* [Shadowsocks8](http://ss8.6gg6.net/)
This website has alreadly been GFWed, it is not accessable without using a VPN.

### Purchasing Accounts
* SScat
Register link: <https://rbq.cat/index/register/>

### Build your own Accounts
I don't know how to do that. Google will help. `:)`