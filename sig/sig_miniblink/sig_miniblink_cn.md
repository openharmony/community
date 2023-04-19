# SIG_MiniBlink
简体中文 | [English](./sig_miniblink.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
1. 做系统级公共渲染组件，对外可提供两套接口，一个用于系统自身，一个用于APP
2. 针对OpenHarmony多平台多内核特性，提供不同级别的渲染能力，包括：
   * 不同的js引擎切换
   * 不同的H5标准支持
   * 不同的拓展能力支持（基础渲染、webgl、webRtc、音视频等）
   * 其他应用场景适配

### 工作范围
1. 定期发布技术分析文章，针对核心代码的编写技巧、算法、架构设计等方面做分享
2. 以单元测试代码为基础，单独封装成小工具或小SDK库，免费开放给社区开发者使用
3. 定期为网友答疑或共同讨论渲染内核相关技术
4. 发布一系列基于MB的不同应用场景的demo，如作为界面库、爬虫库、通用登录模块、通用支付组件等
5. 关于H5标准的讨论
6. 编辑相关书籍，目前市面上一本关于blink的书都没有，计划写两本，一本完全针对内核，一本针对如何优化js写给前端开发者


## 代码仓
- 代码仓地址：

## SIG组成员

### Leader

- [@ampereufo](https://gitee.com/ampereufo)

### Committers列表

- [@nickehu](https://gitee.com/nickehu)
- [@weolar](https://gitee.com/weolar)
- [@Cai_Huan](https://gitee.com/Cai_Huan)


### 会议
 - 会议时间：双周例会，周一晚上19:15，UTC+8
 - 会议申报：
 - 会议链接: Welink或其他会议
 - 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/sig_miniblink.openharmony.io/)邮件列表 [sig_miniblink@openharmony.io](https://lists.openatom.io/postorius/lists/sig_miniblink.openharmony.io/) 获取会议链接
 - 会议纪要: [归档链接地址](https://gitee.com/openharmony-sig/sig-content/tree/master/miniblink/meetings)

### 联系方式(可选)

- 邮件列表：[sig_miniblink@openharmony.io](https://lists.openatom.io/postorius/lists/sig_miniblink.openharmony.io/)
- Zulip群组：https://zulip.openharmony.cn
- 微信群：
