# sig_Qt
简体中文 | [English](./sig_qt.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

Qt SIG负责完成在OpenHarmony的Qt (https://qt.io) 软件开发框架的移植及适配，同时提供基于Qt Creator的OpenHarmony应用程序开发模板及配套开发工具，实现基于Qt研发的应用迁移及OpenHarmony的研发生态补充，将适配OpenHarmony平台的Qt代码提交到Qt社区。

### 工作范围

- Qt SDK模块适配及移植
- Qt Creator配套开发工具插件

Qt框架移植与适配计划贡献内容如下所示：

![Qt框架移植与适配计划贡献内容](figures/qt_oh_framework.png)

### 工作交付件及工作计划
- 2022年10月~2022年12月：完成Qt Core、Qt GUI、Qt QML等核心模块移植适配
- 2022年12月~2023年3月：移植Qt相关的工具，匹配Qt相关的项目工程;完成Qt附加模块移植
- 2023年3月~2023年6月：Qt示例及Demo移植适配验证;Qt单元测试移植适配验证;Qt Creator鸿蒙应用程序模板开发
- 2023年6月~2023年12月：基于Qt API封装鸿蒙系统特性库，引入鸿蒙软总线等系统特性;Qt Creator 鸿蒙应用部署开发;Qt Creator 鸿蒙模拟器开发

## 代码仓
- 代码仓地址：
  - Qt代码仓地址：https://gitee.com/openharmony-sig/qt

## SIG组成员

### Leader
- @cwc1987(https://gitee.com/cwc1987)

### Committers列表
- @zhu.wei(https://gitee.com/zhuwei12345678)
- @xiecy(https://gitee.com/xiecyong)
- @wanglz(https://gitee.com/wanglz1988)
- @wangh(https://gitee.com/CplusCplus)
- @honglianglin(https://gitee.com/honglianglin)


### 会议
 - 会议时间：双周例会，周二 10:00-10:30
 - 会议申报：[Qt SIG议题申报](https://shimo.im/sheets/vVqRVBewOBUx7oqy/MODOC)
 - 会议链接：[WeLink](https://bmeeting.huaweicloud.com:36443/#/j/989208653)
 - 会议通知：请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接
 - 会议纪要：[归档链接地址](https://gitee.com/openharmony-sig/sig-content/tree/master/qt/meetings)
