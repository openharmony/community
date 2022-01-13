# SIG-Telephony
简体中文 | [English](./sig_telephony.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
- 提供SIM卡、搜网、蜂窝数据、蜂窝通话、短彩信等蜂窝移动网络基础通信能力，可管理多类型通话和数据网络连接，为应用开发者提供便捷一致的通信API。

### 工作范围
- 核心服务模块：主要功能是初始化RIL管理、SIM卡和搜网模块。
- 通话管理模块：主要功能是管理CS（Circuit Switch，电路交换）、IMS（IP Multimedia Subsystem，IP多媒体子系统）和OTT（over the top，OTT解决方案）三种类型的通话，申请通话所需要
- 的音视频资源，处理多路通话时产生的各种冲突。
- 蜂窝通话模块：主要功能是实现基于运营商网络的基础通话。
- 短彩信模块：主要功能是短信收发和彩信编解码。
- 状态注册模块：主要功能是提供电话服务子系统各种消息事件的订阅以及取消订阅的API。

## 代码仓
- 代码仓地址：
  - 核心服务：https://gitee.com/openharmony/telephony_core_service
  - 蜂窝通话：https://gitee.com/openharmony/telephony_cellular_call
  - 通话管理：https://gitee.com/openharmony/telephony_call_manager
  - 注册服务：https://gitee.com/openharmony/telephony_state_registry
  - 短彩信：https://gitee.com/openharmony/telephony_sms_mms
  - riladapter：https://gitee.com/openharmony/telephony_ril_adapter
  - 数据业务：https://gitee.com/openharmony/telephony_cellular_data
  - 数据存储：https://gitee.com/openharmony/telephony_data_storage
  - 网络管理：https://gitee.com/openharmony/communication_netmanager_standard
  - 网络协议栈：https://gitee.com/openharmony/communication_netstack
  - 网络管理基础仓：https://gitee.com/openharmony/communication_netmanager_base
  - 网络管理扩展仓：https://gitee.com/openharmony/communication_netmanager_ext


## SIG组成员

### Leader
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)

### Committers列表
- @zhang-hai-feng (https://gitee.com/zhang-hai-feng)
- @jyh926 (https://gitee.com/jyh926)
- @clevercong (https://gitee.com/clevercong)
- @ohos-lsw (https://gitee.com/ohos-lsw)
- @xautosoft (https://gitee.com/xautosoft)
- @hwlitao (https://gitee.com/hwlitao)

### 会议
 - 会议时间：双周例会 周四下午16:00-17:00
 - 会议申报：[SIG-Telephony Meeting Proposal](https://shimo.im/sheets/wgwGRwc9KCYH6Txv/MODOC)
 - 会议链接: Welink或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接
 - 会议纪要: [归档链接地址](https://gitee.com/openharmony-sig/sig-content)

### 联系方式(可选)

- 邮件列表：dev@openharmony.io
- Slack群组：https://zulip.openharmony.cn/
- 微信群：NA
