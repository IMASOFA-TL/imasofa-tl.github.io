---
title: 偶像大师-OFA DISC版本 Patch说明
author: AaronP
tags:
  - Tutorial
---

# 偶像大师-OFA DISC 汉化Patch说明

本教程为偶像大师OFA汉化补丁操作步骤说明。

如遇到问题、希望进行反馈、亦或是有什么建议，请加入测试QQ群：591676099

[微云分流地址](https://share.weiyun.com/SDJaXOmH)

## 目录
- [补丁说明](#%E8%A1%A5%E4%B8%81%E8%AF%B4%E6%98%8E)
- [测试说明](#%E6%B5%8B%E8%AF%95%E8%AF%B4%E6%98%8E)
- [DISC补丁说明](#disc%E8%A1%A5%E4%B8%81%E8%AF%B4%E6%98%8E)
  - [1. 安装原版镜像游戏](#1-%E5%AE%89%E8%A3%85%E5%8E%9F%E7%89%88%E9%95%9C%E5%83%8F%E6%B8%B8%E6%88%8F)
  - [2 准备目录](#2-%E5%87%86%E5%A4%87%E7%9B%AE%E5%BD%95)
  - [3. 运行批处理文件](#3-%E8%BF%90%E8%A1%8C%E6%89%B9%E5%A4%84%E7%90%86%E6%96%87%E4%BB%B6)
  - [4. 覆盖原文件](#4-%E8%A6%86%E7%9B%96%E5%8E%9F%E6%96%87%E4%BB%B6)
  - [5. EBOOT Patch*](#5-eboot-patch)
    - [注意](#%E6%B3%A8%E6%84%8F)
  - [补丁文件SHA1哈希](#%E8%A1%A5%E4%B8%81%E6%96%87%E4%BB%B6sha1%E5%93%88%E5%B8%8C)



## 补丁说明

- 目前补丁暂时只支持汉化DISC版本游戏
- 目前汉化内容大致可供游玩游戏内16周，大约5小时的游戏时间
- 目前主要汉化对象为天海春香、如月千早、星井美希和四条贵音。请按此培育顺序进行试玩
- 补丁适配安装全DLC目录1-14，ver1.07游戏版本，低版本或DLC安装不全可能会出现补丁未生效问题
- RPCS3建议不修改任何画面设置，已证实调整画面和滤镜设置可能导致游戏贴图渲染错误。

## 测试说明

- Patch操作仅支持在Windows10 x64及以上版本操作系统上进行，可能需要.net core3.1 环境，可根据提示自动安装
- 强烈建议组内成员试玩时全程录制，跟踪存档
- 遇到已汉化人物的未汉化文本时，记录信息，并根据录像在群中提供报告
- 遇到错别字，语病或语义错误，请一并记录反馈
- 请使用RPCS3或者PS3实机运行游戏


## DISC补丁说明

> 请仔细阅读，严格按照步骤进行汉化补丁覆盖

### 1. 安装原版镜像游戏

安装原版DISC镜像（BLJS10260），安装ver1.07升级包，1-14全DLC目录。

- HDD DISC文件

  在`games/THE iDOLM@STER One For All [BLJS10260]/PS3_GAME/USRDIR`目录下，应有4项文件（不用关心其他文件和子目录）

  - hdd.arc
  - hdd.bin
  - disc.arc
  - disc.bin

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

### 2 准备目录

新建一个全英文名称文件夹，注意文件夹前缀目录依然是全英文，不要带有中文或全角字符。

如`G:\IMAS-OFA-TLP\ImasOFAProject\Patch\PatchToARC`

在文件夹内新建4个目录

- original
- original_dlc
- patched
- patched_dlc

复制群内发布的补丁执行程序`imas.exe, Imas-Archive.exe`到本目录

复制群内发布的补丁压缩包`patch_main.zip, patch_dlc.zip`到本目录

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

按序依次执行（当前用户，无需开启管理员权限）批处理脚本`patch_main_disc.bat, patch_dlc.bat`，注意执行完成前一个脚本后再执行下一个，不报错的情况下会在`patched`目录和`patched_dlc`目录中得到汉化后的游戏文件



### 4. 覆盖原文件

将`patched`目录中的

- hdd.arc
- hdd.bin
- disc.arc
- disc.bin

覆盖游戏安装目录的HDD DISC文件；

将`patched`目录中的

- _patch.arc.edat
- _patch.bin.edat

和`patched_dlc`目录中的所有文件覆盖硬盘安装目录的EDAT文件。此时你已经完成偶像大师-OFA全部汉化Patch操作。

启动RPCS3或PS3实机，进入游戏，如果UI和文本正常显示中文即代表汉化成功。

### 5. EBOOT Patch*

> EBOOT Patch为可选Patch，针对部分系统UI内容进行汉化，PS3实机需要自行进行重签名，建议RPCS3测试进行此步操作。
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
- 重启游戏

#### 注意

- EBOOT Patch目前仅支持RPCS3，PS3实机需要自行进行重签名。
- 替换后RPCS3会重建SPU Cache，第一次加载可能较慢，且可能有贴图错误。



### 补丁文件SHA1哈希

NULL

