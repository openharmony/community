# SIG_DataManagement
简体中文 | [English](./sig_distributeddatamgr.md)

说明：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](../../zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标
构建面向1+8+N设备全场景的分布式数据管理框架，为开发者提供便捷、高效、稳定、安全的数据管理相关服务

### 工作范围
本地数据库、分布式数据库、数据管理服务等

分布式数据管理SIG（ sig_distributeddatamgr ）技术栈范围全景图如下图所示：
![OpenHarmony文档概览](figures/distributeddatamgr_overview.png)
## 代码仓
|部件名称|部件功能描述|部件仓名称|
| ------------ | ------------ |------------ |
|首选项|支持以XML格式存储和读取用户首选项|distributeddatamgr_preferences|
|关系型数据管理|提供关系型数据数的添加、查询、修改、删除、订阅通知等基本的数据能力|distributeddatamgr_relational_store|
|跨应用数据分享|提供发现应用的能力以及添加、查询、修改、删除数据的标准接口|distributeddatamgr_data_share|
|键值型数据管理|提供键值型数据数的添加、查询、修改、删除、订阅通知等基本的数据能力|distributeddatamgr_kv_store|
|数据管理服务|提供键值型数据库、关系型数据库、持久化对象的跨设备同步能力|distributeddatamgr_datamgr_service|
|分布式数据对象|提供面向对象的内存数据管理框架，向应用开发者提供内存对象的创建、查询、删除、修改、订阅等基本数据对象的管理能力，同时具备分布式能力|distributeddatamgr_data_object|
|剪贴板|提供剪切和拖放数据读写接口，支持身份校验和跨设备剪贴和拖放|miscservices_pasteboard|
|三方开源软件sqlite|提供基础的SQLite库|third_party_sqlite|

## SIG组成员

### Leader
- @gong-a-shi(https://gitee.com/gong-a-shi)

### Committers列表
- @wbq_sky(https://gitee.com/wbq_sky)
- @purple-ding-gags(https://gitee.com/purple-ding-gags)

### 会议
 - 会议时间：每周三 14:15
 - 会议链接：Welink
 - 会议纪要：查看往期会议纪要，请点此[链接](https://gitee.com/openharmony-sig/sig-content/tree/master/distributeddatamgr/meetings)

### 联系方式(可选)

- 邮件列表：dev@openharmony.io
- 微信群：NA
