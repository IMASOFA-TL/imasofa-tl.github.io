---
title: 偶像大师-OFA PSN 汉化补丁说明
author: AaronP
tags:
  - Tutorial
---

# 偶像大师-OFA PSN 汉化补丁说明

本教程为偶像大师OFA汉化补丁PSN版本操作步骤说明。主要服务于实机玩家。

如遇到问题、希望进行反馈、亦或是有任何建议，请加入测试QQ群：591676099

以下是补丁文件分流下载地址👇

- [腾讯微云（26.07.01-已更新）](https://share.weiyun.com/SDJaXOmH)
- [百度网盘（26.07.01-已更新）](https://pan.baidu.com/s/1bjQulu6yb00Lj10j2HLrjA?pwd=r4te)，提取码：r4te
- [Microsoft OneDrive](https://1drv.ms/f/c/609ba33715b5b78e/Ek0mSasszjpJkMTBmgv7R4gBTvyAE5oGk39QxuoLxoYLpA?e=FLi6mN)


## 目录



## 全部所需文件SHA1哈希

请参照[游戏安装说明](https://ofa.idolmaster.top/2025/07/18/InstallTutorial.html)安装好原版PSN镜像（NPJB00611），ver1.07升级包，1-14全DLC目录，并下载汉化组提供的汉化补丁文件和打包程序。以下为本教程使用的文件的SHA1哈希。

### 汉化补丁


- Imas-Archive.exe：5E944D02568B07D9C997A691A7BDFE3B8CCCA236
- imas.exe：E725CC5A43B088575F3E6DCCD0A33932D970766F
- make_npdata.exe：BC751F3EF4DEA8E36CD62BB9A7B7E0519F653005
- patch_main_psn.bat：BA1CC9862FE8E25A8AECD119B45AD70E84C9C4E9
- patch_dlc.bat：92A0BA7EDC916FEDB4441F6BA263C771545E0AFA



## 补丁及游戏说明

- 目前补丁支持汉化PSN版本游戏
- 补丁汉化内容涵盖**完整主线和全DLC Mail内容**
- 补丁适配安装全DLC目录1-14，ver1.07游戏版本，低版本或DLC安装不全可能会出现补丁未生效问题
- Patch操作**仅支持在Windows10 x64及以上版本操作系统**上进行，可能需要`.net core3.1`环境，可根据提示自动安装
- 请使用RPCS3或者PS3实机运行游戏
- RPCS3建议不修改画面设置，已证实调整画面和滤镜设置可能导致游戏贴图渲染错误。
- RPCS3强烈推荐使用**PS3/4/5或PlayStation兼容手柄**，**有线**连接PC进行游戏，Xbox或类Xbox键位手柄**可以游玩但需要自行设置键位映射**，为保证游戏体验顺畅，建议手柄采用**有线连接PC**



## PSN补丁说明

> 请仔细阅读，严格按照步骤进行汉化补丁覆盖

### 1. 安装原版游戏

安装游戏原版pkg，更新pkg和全DLC的pkg

- PSN文件

  在`dev_hdd0\game\NPJB00611\USRDIR`目录下，应有4项文件（不用关心其他文件和子目录）

  - ofa.arc.edat
  - ofa.bin.edat
  - _patch.bin.edat
  - _patch.arc.edat


- EDAT文件

  在`dev_hdd0/game/BLJS10260/USRDIR`下，应有如下文件（注意，虽然PSN版本游戏编号是NPJB00611，但是安装DLC的目录仍然叫做BLJS10260）

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


### 2. 准备目录

新建一个全英文名称文件夹，注意文件夹前缀目录依然是全英文，不要带有中文或全角字符。

如`G:\IMAS-OFA-TLP\ImasOFAProject\Patch\PatchToARC`

在文件夹内新建4个目录

- original
- original_dlc
- patched
- patched_dlc

复制发布的补丁执行程序`imas.exe, Imas-Archive.exe`和解密密钥`JP0700-NPJB00611_00-0000000000000000.rap`到本目录

复制发布的补丁压缩包`patch_main.zip, patch_dlc.zip`到本目录

复制edat加解密程序`make_npdata.exe`到本目录

复制批处理脚本`patch_dlc.bat, patch_main_psn.bat`到本目录

将步骤1中的`PSN文件`复制到`original`目录

将步骤1中的`EDAT文件`中全部复制到`original_dlc`目录


### 3. 运行批处理文件

按序依次执行（当前用户，无需开启管理员权限，鼠标双击bat文件即为执行）批处理脚本`patch_main_psn.bat, patch_dlc.bat`，注意执行完成前一个脚本后再执行下一个，不报错的情况下会在`patched`目录和`patched_dlc`目录中得到汉化后的游戏文件。




### 4. 覆盖原文件

将`patched`目录中的全部4个文件

- ofa.arc.edat
- ofa.bin.edat
- _patch.bin.edat
- _patch.arc.edat

覆盖模拟器游戏安装目录`dev_hdd0\game\NPJB00611\USRDIR`的PSN文件。


再将`patched`目录中的2个文件

- _patch.arc.edat
- _patch.bin.edat

和`patched_dlc`目录中的所有文件覆盖模拟器硬盘安装目录`dev_hdd0/game/BLJS10260/USRDIR`的EDAT文件。(注意这里复制了patched目录中剩余的2个文件和patched_dlc中的所有文件到硬盘安装目录)

### 5. EBOOT Patch *

> （本步为可选操作）EBOOT Patch针对部分系统UI HardCode内容进行汉化，仅需要进行一次，后续升级除非提供新的EBOOT.BIN，否则不再需要进行此步操作。
>
> 汉化前：
>
> ![BeforeEPatch](/images/BeforeEPatch.jpg)
>
> 汉化后：
>
> ![AfterEPatch](/images/AfterEPatch.jpg)

- 将dev_hdd0/game/BLJS10260/USRDIR/下的EBOOT.BIN重命名为EBOOT.BIN.BAK 以备份
- 复制补丁包提供的EBOOT.BIN，粘贴到dev_hdd0/game/BLJS10260/USRDIR/目录下


此时你已经完成偶像大师-OFA全部汉化Patch操作。


#### EBOOT Patch注意事项

- PS3实机在进行EBOOT Patch时需要自行进行重签名。
- 实体机对EBOOT.BIN重签名时可能需要把EBOOT.BIN重命名为EBOOT.ELF，因为是解密后的文件。
- 替换后RPCS3会重建SPU Cache，第一次加载可能较慢，且可能有贴图错误。游戏一段时间后即可恢复正常。



### 6. 游戏内设置


右键Game List中的偶像大师OFA游戏行，展开启动菜单，单击Boot即可进入游戏。

![Boot](/images/Boot.jpg)

如果UI和文本**全部**正常显示**中文**即代表汉化成功 **（只要下图的文字或者UI部分出现了假名就说明你的汉化步骤出问题了）**

![success](/images/success.jpg)


#### 自动存档

由于游戏存档提示时的提示信息将会调用SYSTEM固件的字体，因此会出现固件提示信息汉字缺失现象，因此**强烈推荐开启游戏内的自动存档，让游戏自动按周保存存档**。

![save](/images/save.jpg)

#### 中文制作人名输入

汉化补丁支持非生僻字的中文制作人名输入，具体方式为启动游戏前，在设置内取消勾选`Use native user interface`

![input1](/images/input1.png)

然后进入游戏，在初次要求输入制作人名时，使用电脑系统的输入法在RPCS3提供的输入框内输入名字

![input2](/images/input2.png)
![input3](/images/input3.png)

如果已经输入过制作人名，则常规方式无法再修改名字。需要删掉文件（并非游戏内删除，而且通过电脑删除整个存档文件），rpcs3的存档文件在`dev_hdd0/home/00000001/savedata/`，有两个存档文件夹`BLJS10260_SAVEDATA`和`BLJS10260_PHOTODATA`，均需要删除（PHOTODATA文件夹如果没有保存过MV或者照片可能不存在）


### 7. 补丁升级

汉化补丁支持兼容存档升级，发布更新修复问题的补丁时，请将步骤2目录中的补丁压缩包`patch_main.zip, patch_dlc.zip`更换为最新补丁，重复步骤3，4即可（直接覆盖旧版汉化游戏文件）


### 8. 其他事项

- 如果之前游玩过日文版游戏，在替换中文补丁游戏后闪退，建议右键 `remove -> remove all caches` 尝试清理所有缓存再尝试。




