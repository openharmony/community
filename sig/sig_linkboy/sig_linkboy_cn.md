# sig_linkboy
简体中文 | [English](./sig_linkboy.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](../../zh/pmc.md)中描述的约定。

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

#### 项目介绍
本项目是对于OpenHamony操作系统的插件扩展, 可以支持linkboy对OpenHarmony进行编程

#### 相关资源

linkboy软件下载: www.linkboy.cc


#### 视频案例(b站):

|No|                类别                 |                                    路径                                          |
|--|-------------------------------------|----------------------------------------------------------------------------------|
|1 |linkboy串口助手调试OpenHarmony开发板 |[b站视频链接](https://www.bilibili.com/video/BV1L34y1d72H?spm_id_from=333.999.0.0)|
|2 |linkboy&OpenHarmony编程仿真(小熊派)  |[b站视频链接](https://www.bilibili.com/video/BV1Rq4y1r7D4?spm_id_from=333.999.0.0)|
|3 |linkboy虚拟遥控器控制OpenHarmony外设 |[b站视频链接](https://www.bilibili.com/video/BV1PT4y1R7cF?spm_id_from=333.999.0.0)|
|4 |linkboy虚拟示波器显示传感器数据波形图|[b站视频链接](https://www.bilibili.com/video/BV1nQ4y1U7zw?spm_id_from=333.999.0.0)|
|5 |OpenHarmony图形化编程-红绿蓝彩灯闪烁 |[b站视频链接](https://www.bilibili.com/video/BV13L4y1Y7Av?spm_id_from=333.999.0.0)|

#### OpenHarmony图形化编程案例展示(md文件):

|No|                 类别                     |                                  路径                                 |
|--|------------------------------------------|-----------------------------------------------------------------------|
|1 |OpenHarmony代码模式编程-1个LED闪烁        |[案例链接](oh/oh6.md)|
|2 |OpenHarmony代码编程模式-按钮控制LED       |[案例链接](oh/oh7.md)|
|3 |OpenHarmony代码编程-多线程                |[案例链接](oh/oh8.md)|
|4 |OpenHarmony开发板驱动数码管显示数字       |[案例链接](oh/oh1.md)|
|5 |OpenHarmony开发板运行俄罗斯方块游戏       |[案例链接](oh/oh2.md)|
|6 |OpenHarmony开发板驱动12864液晶屏显示图片  |[案例链接](oh/oh3.md)|
|7 |OpenHarmony内核功能调用示例-微秒延时      |[案例链接](oh/oh4.md)|
|8 |OpenHarmony开发板开启热点                 |[案例链接](oh/oh5.md)|
|9 |OpenHarmony开发板红外遥控解码             |[案例链接](oh/oh9.md)|

#### 中小学信息技术教学文档案例:

|No|                 类别                          |                                   路径                                 |
|--|-----------------------------------------------|------------------------------------------------------------------------|
|1 |OpenHarmony&linkboy图形化编程课件教学(131页pdf)|[百度网盘 提取码: iqax](https://pan.baidu.com/s/1LWQ0p5JclHPxZjDPIDEtpg)|

#### OH-linkboy-SIG工作进展汇报和资料汇总（不断更新）:

* 2021.8.04-第1次linkboy例会
* 2021.9.30-OH线上发布会
* 2021.10.24-第二届开源论坛暨首期师资培训
* 2021.12.10-开放原子开源基金会-linkboy访谈记录

以上资料汇总打包下载链接: [百度网盘 提取码: mucy](https://pan.baidu.com/s/1KAO-CF-DA4HLF4vicmEECw)


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
 - 会议申报：[sig_linkboy会议申报](https://shimo.im/sheets/sX5pBO7PwFkEsR1D)
 - 会议链接：腾讯会议或其他会议
 - 会议通知：请[订阅](https://lists.openatom.io/postorius/lists/dev@openharmony.io)邮件列表获取会议链接
 - 会议纪要：查看往期会议纪要，请点此[链接](https://gitcode.com/openharmony-sig/sig-content/tree/master/linkboy/meetings)

### 联系方式
- 邮件列表：[dev@openharmony.io](https://lists.openatom.io/postorius/lists/dev@openharmony.io/)
- 微信群：请添加linkboy SIG负责人微信拉入群 (13693200752)
