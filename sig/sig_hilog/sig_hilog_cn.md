# sig_HILOG
简体中文 | [English](./sig_hilog.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
- 针对当前已有日志系统存在的功能缺失、性能较低、资源开销大等问题，成立本SIG，目标是为OpenHarmony设计1个全新的日志系统HiLog，能够存储和管理内核日志、系统日志以及三方日志等各种类型的日志，为系统开发者和应用开发者提供丰富便捷的日志访问功能，同时在日志可靠性、接口时延、以及资源开销等方面具有良好的性能体验。本SIG为基础软件服务SIG([SIG_BasicSoftwareService](https://gitee.com/openharmony/community/tree/master/sig/sig_basicsoftwareservice))的子SIG。

### 工作范围

- 解决日志系统普遍存在的问题：

  * 无隐私管控

  * 无日志流控

  * 不能按业务领域管理日志

  * 写日志IO开销大

  * 落盘性能低，无直接落盘机制
  
- 实现灵活部署：日志系统特性可以随OS按需裁剪
- 实现兼容性：日志系统对轻量系统、小型系统和标准系统同构
- 实现高性能/精简/可靠：接口时延、资源占用以及日志丢失率低于同类系统
- 输出相应的技术文档

## 代码仓
- 代码仓地址：
  - hiviewdfx_hilog：https://gitee.com/openharmony/hiviewdfx_hilog
  - hilogtest：https://gitee.com/openharmony/xts_acts/tree/master/hiviewdfx/hilogtest/libhilogtest

## SIG组成员

### Leader
- [v11985](https://gitee.com/v11985)

### Committers列表
- [yaomanhai](https://gitee.com/yaomanhai)
- [stesen](https://gitee.com/stesen)
- [shenchenkai](shenchenkai@huawei.com)
- [aajwy](https://gitee.com/aajwy)
- [youyouyuai](https://gitee.com/youyouyuai)
- [heartofrainbow](https://gitee.com/heartofrainbow)
- [henglab](https://gitee.com/henglab)
- [pan_qing_lin](https://gitee.com/pan_qing_lin)
- [landwind](https://gitee.com/landwind)


### 会议
 - 会议时间：双周例会，时间待定
 - 会议申报：可参考[PMC例会](https://gitee.com/dongjinguang/community/blob/master/zh/pmc.md#pmc%E4%BC%9A%E8%AE%AE%E9%93%BE%E6%8E%A5)申请方式，提供石墨共享文档链接，便于SIG相关申报人自行申请议题
 - 会议链接: 瞩目或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接
 - 会议纪要: [归档链接地址](https://gitee.com/openharmony-sig/sig-content/tree/master/hilog/meetings)

### 联系方式(可选)

- 邮件列表：dev@openharmony.io
- Zulip群组：https://zulip.openharmony.cn/#narrow/stream/47-hilog_sig
- 微信群：xxx
