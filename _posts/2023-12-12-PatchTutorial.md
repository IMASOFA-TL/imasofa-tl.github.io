---
title: 偶像大师-OFA DISC版本 Patch说明
author: Aaron_nep
tags:
  - Archive
---

偶像大师-OFA DISC 汉化Patch说明

## 补丁说明

- 本教程目前面向汉化组内部成员用于测试
- 目前补丁暂时只支持汉化DISC版本游戏
- 目前汉化内容大致可供游玩游戏内16周，大约5小时的游戏时间
- 目前主要汉化对象为天海春香、如月千早、星井美希和四条贵音。请按此培育顺序进行试玩
- 补丁适配安装全DLC目录1-14，ver1.07游戏版本，低版本或DLC安装不全可能会出现补丁未生效问题
- 未经允许，严禁擅自外泄内测汉化补丁文件！

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

新建一个全英文名称文件夹，注意文件夹前缀目录依然是全英文，不要带有中文或全角字符。如`G:\IMAS-OFA-TLP\ImasOFAProject\Patch\PatchToARC`

在文件夹内新建4个目录

- original
- original_dlc
- patched
- patched_dlc

复制群内发布的补丁执行程序`imas.exe, Imas-Archive.exe`到本目录

复制群内发布的补丁压缩包`patch_main.zip, patch_dlc.zip`

复制edat加解密程序`make_npdata.exe`到本目录

复制批处理脚本`patch_dlc.bat，patch_main_disc.bat`到本目录

将步骤1中的`HDD DISC文件`复制到`original`目录

将步骤1中的`EDAT文件`中的`_patch.arc.edat, _patch.bin.edat`也复制到`original`目录

将步骤1中的`EDAT文件`中全部复制到`original_dlc`目录

 

最终目录如下

![patchtotorial_folderstructure](/images/patchtotorial_folderstructure.jpg)

   

`original`目录如下

![orginal_folder](/images/orginal_folder.jpg)

 

`original_dlc`目录如下

![originaldlc_folder](/images/originaldlc_folder.jpg)

### 运行批处理文件

执行批处理脚本`patch_dlc.bat，patch_main_disc.bat`，不报错的情况下会在两个`patch`目录中得到汉化后的游戏文件



### 覆盖原文件

将`patched`目录中的

- hdd.arc
- hdd.bin
- disc.arc
- disc.bin

覆盖游戏安装目录的HDD DISC文件；将

- _patch.arc.edat
- _patch.bin.edat

和`patched_dlc`目录中的所有文件覆盖硬盘安装目录的EDAT文件




### 补丁文件SHA1哈希

NULL

