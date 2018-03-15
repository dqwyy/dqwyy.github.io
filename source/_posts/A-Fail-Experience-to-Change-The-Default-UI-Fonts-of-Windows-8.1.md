---
title: A Fail Experience to Change The Default UI Fonts of Windows 8.1
categories:
  - IT
tags:
  - en
date: 2017-08-10 22:36:08
icon: fa-font
---
UI fonts will change when you change your display language of your OS. As I know, in Windows 8.1, Chinese (China) uses Microsoft YaHei UI, Chinese (Taiwan) uses Microsoft JhengHei UI and English uses Segoe UI. Now the display language of my OS is English (United States), whose UI font is Segoe UI. Han Characters are displayed as Mainland China style instead of Taiwan style. So I would like to change to UI font to Microsoft JhengHei UI. By searching solutions on the internet, I was recommended to modify the Registry by creating a `.reg` file reads:

```reg
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts]
"Segoe UI (TrueType)"=""
"Segoe UI Bold (TrueType)"=""
"Segoe UI Bold Italic (TrueType)"=""
"Segoe UI Italic (TrueType)"=""
"Segoe UI Light (TrueType)"=""
"Segoe UI Semibold (TrueType)"=""
"Segoe UI Symbol (TrueType)"=""

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontSubstitutes]

"Segoe UI"="Microsoft JhengHei UI"
```

I launched this Registry file and then restart my computer. Then I realised that I didn't succeed. As the screenshots below shows, some became SimSun, some became Japanese style font, some became tofu.

![](https://i.loli.net/2017/08/12/598e9d1cbbd8b.png "SimSun")

![](https://i.loli.net/2017/08/12/598e9d1c09fff.png "tofu")

![](https://i.loli.net/2017/08/12/598e9d1dd7309.png "Japanese style font")

Therefore, I had got to restore the awful UI fonts by another Registry file.

```reg
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Fonts]
"Segoe UI (TrueType)"="segoeui.ttf"
"Segoe UI Black (TrueType)"="seguibl.ttf"
"Segoe UI Black Italic (TrueType)"="seguibli.ttf"
"Segoe UI Bold (TrueType)"="segoeuib.ttf"
"Segoe UI Bold Italic (TrueType)"="segoeuiz.ttf"
"Segoe UI Emoji (TrueType)"="seguiemj.ttf"
"Segoe UI Historic (TrueType)"="seguihis.ttf"
"Segoe UI Italic (TrueType)"="segoeuii.ttf"
"Segoe UI Light (TrueType)"="segoeuil.ttf"
"Segoe UI Light Italic (TrueType)"="seguili.ttf"
"Segoe UI Semibold (TrueType)"="seguisb.ttf"
"Segoe UI Semibold Italic (TrueType)"="seguisbi.ttf"
"Segoe UI Semilight (TrueType)"="segoeuisl.ttf"
"Segoe UI Semilight Italic (TrueType)"="seguisli.ttf"
"Segoe UI Symbol (TrueType)"="seguisym.ttf"
"Segoe MDL2 Assets (TrueType)"="segmdl2.ttf"
"Segoe Print (TrueType)"="segoepr.ttf"
"Segoe Print Bold (TrueType)"="segoeprb.ttf"
"Segoe Script (TrueType)"="segoesc.ttf"
"Segoe Script Bold (TrueType)"="segoescb.ttf"

[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\FontSubstitutes]

"Segoe UI"=-
```

I would be appreciated if someone could help me to change the UI fonts of Windows 8.1.