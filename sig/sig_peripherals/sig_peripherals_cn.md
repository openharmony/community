# SIG_Peripherals

简体中文 | [English](./sig_peripherals.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](../../zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

- 1、完成外设的OpenHarmony系统平台能力构建，支持生态伙伴高效、安全、低成本接入OpenHarmony外设生态
- 2、提供IDE工具/开发板技术支持，支持生态伙伴开发外设驱动及配套应用、生态成果共建共享，快速繁荣OpenHarmony外设生态

### 工作范围

本小组核心工作内容主要为依托OpenHarmony平台构建各品类的外设驱动扩展框架共享共建，支持扩展驱动包全流程（开发/部署/安装/更新/运行/能力开放）生命周期管理，如下常用驱动扩展框架已开源在社区

![OpenHarmony文档概览](figures/peripherals_scope.png)

外设驱动技术栈范围全景图
![OpenHarmony技术栈概览](figures/peripherals_overview.png)

目标用户：
- 设备开发者：如打印机、扫描仪、高拍仪、手写板等外设厂商
- 应用开发者：配套外设的应用软件，如手写绘画软件

## 代码仓

- **peripherals_demo代码仓**

| 外设名称 | 驱动功能描述 | 驱动代码仓 |
| ----------- | --------------- | --------- |
| 打印机 | 提供针对打印机类外设驱动开发样例，功能包括设置打印参数，发送打印请求等。 | peripherals_driver_samples/driver_printer(待孵化) |
| 扫描仪 | 提供针对扫描仪类外设驱动开发样例，功能包括扫描文件，导出文件等。 | 暂未开源 |
| 高拍仪 | 提供针对高拍仪类外设驱动开发样例，功能包括选择摄像头，选择摄像头参数，预览，拍照等。 | peripherals_driver_samples/driver_high-speed_ducument_scanner（待孵化） |
| 手写板 | 提供针对手写板类外设驱动开发样例，功能包括手写板区域设置，手写板按键快捷键设置等功能。 | peripherals_driver_samples/driver_handwriting（待孵化） |
| 鼠标 | 提供针对非标鼠标类外设驱动开发样例，功能包括针对鼠标侧键进行改建等功能。 | peripherals_driver_samples/driver_mouse（待孵化） |
| Ukey | 提供针对银行Ukey类外设驱动开发样例，功能包括查询key信息，校验pin码等。 | peripherals_driver_samples/driver_ukey（待孵化） |

## SIG组成员

### Leader

- @yihaitao(https://gitee.com/yihaitao8686)

### Committers列表

- @lujianying(https://gitee.com/SiWuPan)

- @chenchong(https://gitee.com/cc13335166233)

- @yuanyulu(https://gitee.com/yuan-yulu)

- @fuqing(https://gitee.com/fuqing-sz)

- @huangqiaohua(https://gitee.com/daddykiko)

- @liukuo(https://gitee.com/kuokuozaixian)

- @lixinsheng(https://gitee.com/lixinsheng2)

- @liudimin(https://gitee.com/Danny_liuXu)
  
### 会议
  
  - 会议时间：双周例会，周三下午16:00，UTC+8
  - 会议申报：
  - 会议链接：腾讯会议或其他会议
  - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io/)邮件列表获取会议链接
  - 会议纪要：查看往期会议纪要，请点此[链接](https://gitee.com/openharmony-sig/sig-content)

### 联系方式(可选)

- 邮件列表：dev@openharmony.io
- 微信群：xxx
