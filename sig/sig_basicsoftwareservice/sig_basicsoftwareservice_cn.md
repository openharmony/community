# SIG_BasicSoftwareService 
简体中文 | [English](./sig_basicsoftwareservice.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
为OpenHarmony提供简洁、高效的基础软件服务；通过部件化设计，可组合支撑L0~L5多种不同级别设备的系统软件开发。

BasicSoftwareService SIG技术栈范围全景图如下图所示：

![image-20220722232522588](./images/overview_zh.png)

### 工作范围
基础软件服务主要包括以下几个子系统：
| 名称|说明|
| :----- | :----- |
|启动子系统|提供系统OS系统启动框架，包括系统引导过程，init初始进程管理以及系统参数属性机制|
|升级服务子系统|提供系统升级能力|
|DFX子系统|提供DFT、DFR、DFM等系统能力|
|账号子系统|提供系统的账号管理能力|
|无障碍软件服务子系统|提供无障碍软件服务能力|
|定制子系统|提供系统定制化能力，包括基于配置层级的定制框架、企业环境下的设备管理和定制化设置等|
|时间时区子系统|提供管理系统时间时区和定时的能力，支持设置获取时间、日期、时区和系统定时器功能|
|主题框架子系统|提供壁纸管理服务能力，支持系统显示、设置、切换壁纸等功能，以及锁屏管理服务|
|输出法框架子系统|提供输入法开发框架，供输入法应用使用，以及提供输入法管理接口|
|上传下载子系统|向三方应用提供系统下载/上传服务能力|
|打印子系统|支持三方应用创建打印任务，拉起后台打印任务管理，管理打印扩展和打印任务；支持三方应用发现和连接扫描仪，设置扫描参数，启动扫描和获取扫描图片|


## SIG组成员

### Leader
- @handyohos(https://gitee.com/handyohos)


### 会议
 - 会议时间: 双周三 14:00
 - 会议申报: [OpenHarmony sig_BasicSoftware Meeting Proposal](https://etherpad.openharmony.cn/p/sig_basicsoftware)
 - 会议链接: Welink

### 联系方式(可选)

- 邮件列表：dev@openharmony.io
- 微信群：NA
