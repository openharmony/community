# SIG-linkboy
简体中文 | [English](./sig_linkboy.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
* 技术层面：联合志愿者协同开展后续linkboy对OpenHarmony系统的适配和移植
* 应用层面：基于linkboy社区的已有用户群，推广OpenHarmony系统

### 工作范围
* 编译器后端指令集适配
* 完善linkboy组件适配
* OpenHarmony组件图形化封装
* OpenHarmony组件仿真支持
* 各厂家OpenHarmony开发板图形化封装


## 代码仓
- 代码仓地址：
  - linkboy：https://gitee.com/openharmony-sig/linkboy

#### 项目介绍
本项目是对于OpenHamony操作系统的插件扩展, 可以支持linkboy对OpenHarmony进行编程

#### 相关资源

linkboy软件下载: www.linkboy.cc

linkboy&OpenHarmony简介: https://bbs.elecfans.com/jishu_2118283_1_1.html

linkboy&OpenHarmony编程（基础篇）教程: https://bbs.elecfans.com/group_1537

linkboy&OpenHarmony相关案例视频: https://space.bilibili.com/547895278

linkboy-SIG代码仓：https://gitee.com/openharmony-sig/linkboy

linkboy SIG 历次会议纪要：https://gitee.com/openharmony-sig/sig-content/tree/master/linkboy/meetings

#### 软件架构
本项目包含: 
1.  OpenHarmony功能的封装 (HAL: GPIO, UART, TIMER, ...)
2.  提供一个精简的虚拟机实现, 可以运行linkoby编程语言的后端字节码序列
3.  包含一些特殊类的驱动程序, 如: 红外解码, 步进电机驱动, 温湿度DS18B20, DHT系列...

#### 使用说明

1.  将vos文件夹放置于 OpenHarmony 源码的 Application\sample\wifi-iot\app 文件夹;
2.  将父文件夹的 BUILD.gn 文件内容改为:

import("//build/lite/config/component/lite_component.gni")
lite_component("app") {
    features = [
        "vos:main"
    ]
}

#### 开发路标规划

1. 增加完善OpenHarmony L0 通信类扩展库的图形化封装;
2. 增加对OpenHarmony L1/L2 体系的VOS虚拟机移植适配;
3. 增加OpenHarmony生态合作伙伴的开发板图形化编程支持;

## SIG组成员

### Leader
- [linkboy_crux](https://gitee.com/linkboy_crux)

### Committers列表
- [lcm](https://gitee.com/lcm)
- [chaoyangc](https://gitee.com/chaoyangc)
- [ownery](https://gitee.com/ownery)

### 会议
 - 会议时间：双周例会，周五 20:00
 - 会议申报：[SIG-linkboy会议申报](https://shimo.im/sheets/sX5pBO7PwFkEsR1D)
 - 会议链接：腾讯会议或其他会议
 - 会议通知：请[订阅](https://lists.openatom.io/postorius/lists/sig_linkboy.openharmony.io)邮件列表获取会议链接
 - 会议纪要：查看往期会议纪要，请点此[链接](https://gitee.com/openharmony-sig/sig-content/tree/master/linkboy/meetings)

### 联系方式(可选)

- 邮件列表：[sig_linkboy@openharmony.io](https://lists.openatom.io/postorius/lists/sig_linkboy.openharmony.io/)
- Zulip群组：https://zulip.openharmony.cn
- 微信群：xxx
