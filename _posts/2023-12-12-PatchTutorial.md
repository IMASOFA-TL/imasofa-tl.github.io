---
title: 偶像大师-OFA DISC 汉化补丁说明
author: AaronP
tags:
  - Tutorial
---

# 偶像大师-OFA DISC 汉化补丁说明

本教程为偶像大师OFA汉化补丁操作步骤说明。

如遇到问题、希望进行反馈、亦或是有任何建议，请加入测试QQ群：591676099

以下是补丁文件分流下载地址👇

- [腾讯微云](https://share.weiyun.com/SDJaXOmH)
- [Microsoft OneDrive](https://1drv.ms/f/c/609ba33715b5b78e/Ek0mSasszjpJkMTBmgv7R4gBTvyAE5oGk39QxuoLxoYLpA?e=FLi6mN)
- [百度网盘](https://pan.baidu.com/s/1g8DxLewfTgThfGkG4jyzEA?pwd=IMAS)，提取码：IMAS
- [阿里云盘](https://www.alipan.com/s/9BxwWct4btg)，提取码: zw78
- [夸克网盘](https://pan.quark.cn/s/3f98c3a721fd?pwd=FRPL)，提取码：FRPL


## 目录

- [偶像大师-OFA DISC 汉化补丁说明](#%E5%81%B6%E5%83%8F%E5%A4%A7%E5%B8%88-ofa-disc-%E6%B1%89%E5%8C%96%E8%A1%A5%E4%B8%81%E8%AF%B4%E6%98%8E)
  - [目录](#%E7%9B%AE%E5%BD%95)
  - [全部所需文件SHA1哈希](#%E5%85%A8%E9%83%A8%E6%89%80%E9%9C%80%E6%96%87%E4%BB%B6sha1%E5%93%88%E5%B8%8C)
    - [汉化补丁](#%E6%B1%89%E5%8C%96%E8%A1%A5%E4%B8%81)
  - [补丁及游戏说明](#%E8%A1%A5%E4%B8%81%E5%8F%8A%E6%B8%B8%E6%88%8F%E8%AF%B4%E6%98%8E)
  - [DISC补丁说明](#disc%E8%A1%A5%E4%B8%81%E8%AF%B4%E6%98%8E)
    - [1. 安装原版镜像游戏](#1-%E5%AE%89%E8%A3%85%E5%8E%9F%E7%89%88%E9%95%9C%E5%83%8F%E6%B8%B8%E6%88%8F)
    - [2. 准备目录](#2-%E5%87%86%E5%A4%87%E7%9B%AE%E5%BD%95)
    - [3. 运行批处理文件](#3-%E8%BF%90%E8%A1%8C%E6%89%B9%E5%A4%84%E7%90%86%E6%96%87%E4%BB%B6)
    - [4. 覆盖原文件](#4-%E8%A6%86%E7%9B%96%E5%8E%9F%E6%96%87%E4%BB%B6)
    - [5. EBOOT Patch](#5-eboot-patch)
      - [EBOOT Patch注意事项](#eboot-patch%E6%B3%A8%E6%84%8F%E4%BA%8B%E9%A1%B9)
    - [6. 游戏内设置](#6-%E6%B8%B8%E6%88%8F%E5%86%85%E8%AE%BE%E7%BD%AE)
    - [7. 补丁升级](#7-%E8%A1%A5%E4%B8%81%E5%8D%87%E7%BA%A7)

## 全部所需文件SHA1哈希

请参照[游戏安装说明](https://imas-ofa.com/2025/07/18/InstallTutorial.html)安装好原版DISC镜像（BLJS10260），ver1.07升级包，1-14全DLC目录，并下载汉化组提供的汉化补丁文件和打包程序。以下为本教程使用的文件的SHA1哈希。

### 汉化补丁

- patch_main.zip：07092C346B4A34676D1788110A27CB7DE9AB07C5 （更新补丁请参考对应发布页哈希）
- patch_dlc.zip：F7AAB1039DA2D5AFAA554A2B3702C9218148E3F9 （更新补丁请参考对应发布页哈希）
- EBOOT.BIN：8FEAC512508BCA93F1CBD32F458FCF40A0C976B6
- Imas-Archive.exe：5E944D02568B07D9C997A691A7BDFE3B8CCCA236
- imas.exe：E725CC5A43B088575F3E6DCCD0A33932D970766F
- make_npdata.exe：BC751F3EF4DEA8E36CD62BB9A7B7E0519F653005
- patch_main_disc.bat：42B901EE6A3FDD027C62810B8B268D7F0BE1052B
- patch_dlc.bat：92A0BA7EDC916FEDB4441F6BA263C771545E0AFA



## 补丁及游戏说明

- 目前补丁支持汉化DISC版本游戏
- 补丁汉化内容涵盖**完整主线和全DLC Mail内容**
- 补丁适配安装全DLC目录1-14，ver1.07游戏版本，低版本或DLC安装不全可能会出现补丁未生效问题
- Patch操作**仅支持在Windows10 x64及以上版本操作系统**上进行，可能需要`.net core3.1`环境，可根据提示自动安装
- 请使用RPCS3或者PS3实机运行游戏
- RPCS3建议不修改画面设置，已证实调整画面和滤镜设置可能导致游戏贴图渲染错误。
- RPCS3强烈推荐使用**PS3/4/5或PlayStation兼容手柄**，**有线**连接PC进行游戏，Xbox或类Xbox键位手柄**可以游玩但需要自行设置键位映射**，为保证游戏体验顺畅，建议手柄采用**有线连接PC**



## DISC补丁说明

> 请仔细阅读，严格按照步骤进行汉化补丁覆盖

### 1. 安装原版镜像游戏

参照[游戏安装说明](https://imas-ofa.com/2025/07/18/InstallTutorial.html)安装好原版DISC镜像（BLJS10260），ver1.07升级包，1-14全DLC目录（这里假定你的游戏目录为`THE iDOLM@STER One For All [BLJS10260]`）

- HDD DISC文件

  在`games/THE iDOLM@STER One For All [BLJS10260]/PS3_GAME/USRDIR`目录下，应有4项文件（不用关心其他文件和子目录）

  - hdd.arc
  - hdd.bin
  - disc.arc
  - disc.bin

  ![GAMEDIR](/images/GAMEDIR.jpg)


- EDAT文件

  在`dev_hdd0/game/BLJS10260/USRDIR`下，应有如下文件

  - _patch.arc.edat
  - _patch.bin.edat
  - dlc01.arc.edat, dlc01.bin.edat
  - dlc02.arc.edat, dlc02.bin.edat
  - _dlc03.arc.edat, _dlc03.bin.edat
  - _dlc04.arc.edat, _dlc04.bin.edat
  - _dlc05.arc.edat, _dlc05.bin.edat
  - _dlc06.arc.edat, _dlc06.bin.edat
  - _dlc07.arc.edat, _dlc07.bin.edat
  - _dlc08.arc.edat, _dlc08.bin.edat
  - _dlc09.arc.edat, _dlc09.bin.edat
  - _dlc10.arc.edat, _dlc10.bin.edat
  - _dlc11.arc.edat, _dlc11.bin.edat
  - _dlc12.arc.edat, _dlc12.bin.edat
  - _dlc13_107.arc.edat, _dlc13_107.bin.edat
  - _dlc14_107.arc.edat, _dlc14_107.bin.edat

  ![HDDDIR](/images/HDDDIR.jpg)


### 2. 准备目录

新建一个全英文名称文件夹，注意文件夹前缀目录依然是全英文，不要带有中文或全角字符。

如`G:\IMAS-OFA-TLP\ImasOFAProject\Patch\PatchToARC`

在文件夹内新建4个目录

- original
- original_dlc
- patched
- patched_dlc

复制发布的补丁执行程序`imas.exe, Imas-Archive.exe`到本目录

复制发布的补丁压缩包`patch_main.zip, patch_dlc.zip`到本目录

复制edat加解密程序`make_npdata.exe`到本目录

复制批处理脚本`patch_dlc.bat, patch_main_disc.bat`到本目录

将步骤1中的`HDD DISC文件`复制到`original`目录

将步骤1中的`EDAT文件`中的`_patch.arc.edat, _patch.bin.edat`也复制到`original`目录

将步骤1中的`EDAT文件`中全部复制到`original_dlc`目录

 

最终目录如下

![patchtotorial_folderstructure](/images/patchtotorial_folderstructure.jpg)

   

`original`目录如下

![orginal_folder](/images/orginal_folder.jpg)

 

`original_dlc`目录如下

![originaldlc_folder](/images/originaldlc_folder.jpg)

### 3. 运行批处理文件

按序依次执行（当前用户，无需开启管理员权限）批处理脚本`patch_main_disc.bat, patch_dlc.bat`，注意执行完成前一个脚本后再执行下一个，不报错的情况下会在`patched`目录和`patched_dlc`目录中得到汉化后的游戏文件，下图为正确自行完成的图示。

![patchcmd](/images/patchcmd.jpg)

![patchdlccmd](/images/patchdlccmd.jpg)

其中`patched`目录有6个文件，`patched_dlc`目录有28个文件

![patched](/images/patched.jpg)

![patched_dlc](/images/patched_dlc.jpg)


### 4. 覆盖原文件

将`patched`目录中的以下4个文件

- hdd.arc
- hdd.bin
- disc.arc
- disc.bin

覆盖模拟器游戏安装目录`games/THE iDOLM@STER One For All [BLJS10260]/PS3_GAME/USRDIR`的HDD DISC文件。(注意不包括_patch.arc.edat和_patch.bin.edat)


再将`patched`目录中的剩下的以下2个文件

- _patch.arc.edat
- _patch.bin.edat

和`patched_dlc`目录中的所有文件覆盖模拟器硬盘安装目录`dev_hdd0/game/BLJS10260/USRDIR`的EDAT文件。(注意这里复制了patched目录中剩余的2个文件和patched_dlc中的所有文件到硬盘安装目录)

### 5. EBOOT Patch

> EBOOT Patch针对部分系统UI HardCode内容进行汉化，仅需要进行一次，后续升级除非提供新的EBOOT.BIN，否则不再需要进行此步操作。
>
> 汉化前：
>
> ![BeforeEPatch](/images/BeforeEPatch.jpg)
>
> 汉化后
>
> ![AfterEPatch](/images/AfterEPatch.jpg)

- 将dev_hdd0/game/BLJS10260/USRDIR/下的EBOOT.BIN重命名为EBOOT.BIN.BAK 以备份
- 复制本目录下的EBOOT.BIN，粘贴到dev_hdd0/game/BLJS10260/USRDIR/目录下


此时你已经完成偶像大师-OFA全部汉化Patch操作。


#### EBOOT Patch注意事项

- PS3实机在进行EBOOT Patch时需要自行进行重签名。
- 替换后RPCS3会重建SPU Cache，第一次加载可能较慢，且可能有贴图错误。游戏一段时间后即可恢复正常。



### 6. 游戏内设置


右键Game List中的偶像大师OFA游戏行，展开启动菜单，单击Boot即可进入游戏，如果UI和文本正常显示中文即代表汉化成功。

![Boot](/images/Boot.jpg)


由于游戏存档提示时的提示信息将会调用SYSTEM固件的字体，因此会出现固件提示信息汉字缺失现象，因此**强烈推荐开启游戏内的自动存档，让游戏自动按周保存存档**。

![save](/images/save.jpg)

### 7. 补丁升级

汉化补丁支持兼容存档升级，发布更新修复问题的补丁时，请将步骤2目录中的补丁压缩包`patch_main.zip, patch_dlc.zip`更换为最新补丁，重复步骤3，4即可（直接覆盖旧版汉化游戏文件）



