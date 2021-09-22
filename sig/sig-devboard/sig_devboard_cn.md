# SIG_DevBoard
简体中文 | [English](./sig_devboard.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
- 解决OHOS芯片及板卡移植适配

- 解决OHOS主板及配件的碎片化

- 提供OHOS板卡一站式服务平台

- 提供OHOS板卡商机的交流平台

- 协助OHOS板卡商的代码上库

### 工作范围

- 提供OHOS芯片适配及规划

  - 统计当前已适配、适配中、计划适配芯片的情况与进展

- 提供OHOS板卡的硬件规范

  - 为方便开发板通用性，提出硬件接口规范。建议开发板厂商在此规范下开发、生产、销售

- 易移植性需求

  - 提出移植性需求，所有的OpenHarmony项目都需要支持，不仅是内核和编译项目

- 移植和贡献规范

  - 指导设备厂商、芯片厂商、单板厂商贡献他们的代码、文档到社区

- 样例工程

  - 创建设备厂商、芯片厂商、单板厂商的样例工程，给其他厂商参考

- 生态拓展

  - 积极与设备厂商、芯片厂商、单板厂商进行洽谈合作

## 代码仓
- 代码仓地址：
  - device_st: https://gitee.com/openharmony-sig/device_st
  - vendor_st: https://gitee.com/openharmony-sig/vendor_st
  - device_allwinner: https://gitee.com/openharmony-sig/device_allwinner
  - device_allwinner: https://gitee.com/openharmony-sig/devboard_device_allwinner_XR806
  - vendor_allwinner: https://gitee.com/openharmony-sig/vendor_allwinner
  - vendor_allwinner: https://gitee.com/openharmony-sig/devboard_vendor_allwinner_XR806
  - device_mediatek: https://gitee.com/openharmony-sig/device_mediatek
  - vendor_mediatek: https://gitee.com/openharmony-sig/vendor_mediatek
  - device_nordic: https://gitee.com/openharmony-sig/device_nordic
  - vendor_nordic: https://gitee.com/openharmony-sig/vendor_nordic
  - device_nxp: https://gitee.com/openharmony-sig/device_nxp
  - vendor_nxp: https://gitee.com/openharmony-sig/vendor_nxp
  - device_fudanmicro: https://gitee.com/openharmony-sig/device_fudanmicro
  - vendor_fudanmicro: https://gitee.com/openharmony-sig/vendor_fudanmicro
  - device_bestechnic: https://gitee.com/openharmony-sig/device_bestechnic
  - vendor_bestechnic: https://gitee.com/openharmony-sig/vendor_bestechnic
  - device_ingenic: https://gitee.com/openharmony-sig/device_ingenic
  - vendor_ingenic: https://gitee.com/openharmony-sig/vendor_ingenic
  - device_espressif: https://gitee.com/openharmony-sig/device_espressif
  - vendor_espressif: https://gitee.com/openharmony-sig/vendor_espressif
  - device_winnermicro: https://gitee.com/openharmony-sig/device_winnermicro
  - vendor_winnermicro: https://gitee.com/openharmony-sig/vendor_winnermicro
  - device_rockchip: https://gitee.com/openharmony-sig/device_rockchip
  - vendor_rockchip: https://gitee.com/openharmony-sig/vendor_rockchip
  - device_unisoc: https://gitee.com/openharmony-sig/device_unisoc
  - vendor_unisoc: https://gitee.com/openharmony-sig/vendor_unisoc
  - device_broadcom: https://gitee.com/openharmony-sig/device_broadcom
  - vendor_broadcom: https://gitee.com/openharmony-sig/vendor_broadcom
  - device_realtek: https://gitee.com/openharmony-sig/device_realtek
  - vendor_realtek: https://gitee.com/openharmony-sig/vendor_realtek
  - device_bouffalolab: https://gitee.com/openharmony-sig/device_bouffalolab
  - vendor_bouffalolab: https://gitee.com/openharmony-sig/vendor_bouffalolab
  - device_beken: https://gitee.com/openharmony-sig/device_beken
  - vendor_beken: https://gitee.com/openharmony-sig/vendor_beken
  - device_asrmicro: https://gitee.com/openharmony-sig/device_asrmicro
  - vendor_asrmicro: https://gitee.com/openharmony-sig/vendor_asrmicro
  - device_qemu: https://gitee.com/openharmony/device_qemu
  - vendor_ohemu: https://gitee.com/openharmony/vendor_ohemu
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_device_hihope_build
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_device_hihope_dayu
  - device_hoperun:https://gitee.com/openharmony-sig/devboard_vendor_hihope
  - device_bearpi: https://gitee.com/openharmony-sig/device_bearpi_bearpi_hm_nano
  - device_bearpi:https://gitee.com/openharmony-sig/applications_sample_bearpi_hm_nano
  - device_bearpi:https://gitee.com/openharmony-sig/vendor_bearpi
  - vendor_huawei_ipcamera_v3s: https://gitee.com/openharmony-sig/vendor_huawei_ipcamera_v3s
  - vendor_oh_fun: https://gitee.com/openharmony-sig/vendor_oh_fun
  - vendor_huawei_minidisplay_demo: https://gitee.com/openharmony-sig/vendor_huawei_minidisplay_demo

## SIG组成员

### Leader
- [liuyang198591](https://gitee.com/liuyang198591)

### Committers列表
- [li-gaopeng0312](https://gitee.com/li-gaopeng0312)
- [zianed](https://gitee.com/zianed)
- [DennyShen](https://gitee.com/DennyShen)
- [borne](https://gitee.com/borne)
- [jady3356](https://gitee.com/taiyipei)
- [zeeman_wang](https://gitee.com/zeeman_wang)
- [dxbedu](https://gitee.com/dxbedu)
- [SimonLi](https://gitee.com/kkup180)
- [kefeixiong](https://gitee.com/addyke)
- [cijliu](https://gitee.com/cijliu)
- [Laowang-BearPi](https://gitee.com/laowangiotclub)
- [weidongshan](https://gitee.com/weidongshan)
- [Leon](https://gitee.com/jahyeon)
- [zhao_xiuxiu](https://gitee.com/zhao_xiuxiu)
- [firefly_team](https://gitee.com/firefly_team)

### 会议
 - 会议时间：双周例会，周四上午10:00
 - 会议申报：[SIG-DevBoard会议申报](https://shimo.im/sheets/UZBk8yBk0y4NE4SZ)
 - 会议链接：腾讯会议或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/sig_devboard.openharmony.io/)邮件列表获取会议链接
 - 会议纪要：查看往期会议纪要，请点此[链接](https://gitee.com/openharmony-sig/sig-content/tree/master/devboard/meetings)

### 联系方式(可选)

- 邮件列表：[sig_devboard@openharmony.io](https://lists.openatom.io/postorius/lists/sig_devboard.openharmony.io/)
- Zulip群组：https://zulip.openharmony.cn
- 微信群：xxx
