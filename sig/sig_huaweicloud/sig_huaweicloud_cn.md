# sig_HuaweiCloud
简体中文 | [English](./sig_huaweicloud.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
为OpenHarmony提供云端配合组件，希望华为云能在更多新的方案带动OpenHarmony的突破，促进其生态的发展。

### 工作范围
- 负责承担华为云组件开源软件托管平台职责；
- 负责华为云相关开源项目模块架构设计、评审和决策；
- 负责华为云领域软件模块的代码审核、合入，禁止低质量代码合入开源版本主干，负责测试代码看护；
- 积极有效参与开源社区代码检视与点评，共享编程经验，与开源社区开发者交流，传递软件开发技能，有效辅导开源社区开发者写出好代码；
- 处理开源社区上的需求、issue、邮件列表和开发问题；
- 结合评审和开发活动，给予代码质量反馈与指导，促进开源社区代码质量提升。

## 代码仓

|部件名称<img width=100/>|部件功能描述<img width=200/>|部件仓名称<img width=100/>|
|---|---|---|
| IoT                      | 帮助OpenHarmony轻量系统、小型系统以及标准系统设备快速对接物联网平台，支持TCP/IP协议栈的设备集成IoT Device SDK后，可以直接与物联网平台通信。不支持TCP/IP协议栈的设备，如蓝牙、ZigBee等设备，可以通过集成了IoT Device SDK的网关将设备数据转发给物联网平台，与云平台进行通信。主要的端云协同功能如下：<br>云平台通信能力:与云平台进行建链，断链，消息、属性、事件等上报，以及接收命令、消息下发，文件上传下载等一系列通信功能。<br>端云安全通信：云端下发安全PIN码信息，通过华为云平台下发设备组，设备通过OpenHarmony软总线实现物物互联。<br>设备规则引擎：端侧规则提供与云端规则相似的能力，设置规则后，设备会判断是否满足规则触发条件，在条件满足时，设备会执行用户预设的动作。与云端规则不同，端侧规则可以在网络中断或设备无法与云端交互情况下，继续在端侧运行。<br/>远程SSH登录：可实现通过华为云IoTDA平台远程登录自己在线的设备。<br>异常检测：基于端云协同，实现设备对于诸如内存、存储空间、异常端口、电池电量、CPU占用率等异常检测的功能。<br>M2M功能：目前支持使用SDK对接边缘IoTEdge，边缘节点完成消息的中转到目标设备。 | iot_device_sdk_c<br>iot_device_sdk_c_tiny |

- project name:
  - iot_device_sdk_c: https://gitee.com/openharmony/iot_device_sdk_c
  
  - iot_device_sdk_c_tiny: https://gitee.com/openharmony/iot_device_sdk_c_tiny
  

## SIG组成员

### Leader
- @one_two_zero(https://gitee.com/one_two_zero)

### Committers列表
- @one_two_zero(https://gitee.com/one_two_zero)
- @liteos2021(https://gitee.com/liteos2021)
- @xinglichen(https://gitee.com/xinglichen）
- @jojo_cjw(https://gitee.com/jojo_cjw)
- @Aiminabb(https://gitee.com/Aiminabb)

### 会议
 - 会议时间：双周例会，周四下午14:30-16:00，UTC+8
 - 议题申报: [OpenHarmony sig_HuaweiCloud Meeting Proposal](https://shimo.im/sheets/zdkyBwNxgzCP8nA6/MODOC)
 - 会议链接：Welink或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io) 邮件列表 dev@openharmony.io 获取会议链接
 - 会议纪要：查看往期会议纪要，请点此[会议纪要](https://gitee.com/openharmony-sig/sig-content/tree/master/huaweicloud/meetings)

### 联系方式(可选)
| 地址                                 | 简介        | 用途说明                                                         |
| ---------------------------------------|---------- | ------------------------------------------------------------ |
| dev@openharmony.io  <img width=120/>| 开发邮件列表 <img width=100/> | OpenHarmony社区开发讨论邮件列表，任何社区开发相关话题都可以在邮件列表讨论。任何开发者可[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)。<img width=200/>|
