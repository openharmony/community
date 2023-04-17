## OpenHarmony项目管理委员会（PMC）


   OpenHarmony项目管理委员会（PMC: Project Management Committee）负责OpenHarmony社区管理，职责如下：
1. 负责社区管理工作，包括开源社区版本规划、架构看护、特性代码开发维护、版本及补丁规划等；
2. 发布和处理社区需求，为开源社区提供技术架构指导和技术决策；
3. 处理社区Bug、issue、邮件列表等渠道开发者反馈问题；
4. 负责PMC、Committer成员的[选举和退出](./guidelines_role_growth.md)，制定PMC、Committer协作机制；

## PMC 关键角色职责定义
| 领域     | 职责定义                                                                                                                                                                                                                             | 维护的流程和社区规则                                                          |
| ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- |
| PMC主席  | 负责OpenHarmony社区整体技术治理和管理；<br>主持OpenHarmony社区PMC、Committer新成员的选举和退出，以及社区协作机制；<br>召集和主持PMC会议，并检查PMC会议决议的落实情况；<br>代表PMC或委派PMC成员参与OpenHarmony项目群周边组织会议，以及外部技术交流活动，提升社区影响力。                                                              | 新技术项目引入和孵化流程；<br>软件包选型引入和退出决策流程；<br>社区技术治理和运作规范流程；<br>社区版本GO/NO-GO决策流程。 |
| 架构     | 领域SIG社区管理工作：包括跨领域间技术竞争分析和关键技术识别，SIG领域间接口定义与维护跨SIG间架构设计变更的评审和最终决策；<br>负责跨SIG领域间接口变更的联合评审和决策；<br>架构设计原则制定，架构变更和看护。                                                                                                                  | SIG领域间技术孵化流程；<br>SIG领域间技术决策流程；<br>代码仓新建、孵化、退休和毕业。                      |
| 版本发布   | 规划和计划版本的发行时间表；<br>在开发/测试周期中跟踪（更新updates或功能feature）的开发状态；<br>版本发布协调，参与相关组和发布相关等会议；<br>负责项目的交付过程协调。                                                                                                            | 社区版本发布流程；<br>社区版本发行时间表；<br>社区版本补丁发布流程和生命周期策略说明。                        |
| 质量运营   | 负责SIG项目孵化准出的质量标准制定；<br>负责社区开发、治理、运营等流程规范的制定和发布；<br>制定社区奖惩机制，例行跟踪社区运营问题，并定期在PMC例会汇报关键角色参与社区治理情况；<br>代表质量和合规领域参加OH的技术峰会和布道。                                                                                                            | SIG项目孵化流程规范制定；<br>社区开发、治理和运营等流程规范制定和发布。                               |
| API治理  | 功能性：对API接口的功能负责。包括API能否满足生态系统参与者的需求；<br>可用性：对API的可用性负责。确保在API中表达相似概念的方式上的一致性，有完善的API文档说明，易于开发者学习；<br>治理：该SIG负责向OpenHarmony的贡献者清楚地传达决策和决策依据，决策过程透明化；<br>客户的满意：SIG应该营造一种环境让SIG与API设计人员进行建设性的合作，针对API变更、新增、删除，SIG成员应及时且礼貌地回应API审核的请求。 | 明确的API社区治理规则；<br>完善的API设计规范和优秀实践记录。                                   |
| 基础设施   | 支持社区构建发布工具基础架构/发布工程的工具环境；<br>支持社区工具应用程序维护；<br>支持社区沟通交流和社区运营监控平台；<br>制定社区的基础设施发展计划。                                                                                                                                                   | 构建工具使用指导；<br>社区通信使用指导。                                                |
| 基础软件服务 | OH基础软件服务相关的技术竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责基础软件服务领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责基础软件服务领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表基础软件服务领域参加OH的技术峰会和布道。                                                              | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 内核     | 核和文件系统相关的技术竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责内核和文件系统相关领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责内核和文件系统相关领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表内核和文件系统相关领域参加OH的技术峰会和布道。                                                       | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 编译运行时  | 编译运行时技术领域竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责编译运行时技术领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责编译运行时技术领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表编译运行时技术领域参加OH的技术峰会和布道。                                                               | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 驱动框架   | 驱动框架技术领域的竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责驱动框架技术领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责驱动框架技术领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表负责驱动框架技术领域参加OH的技术峰会和布道。                                                                | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 安全架构   | 安全领域内的技术竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责安全领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责安全领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表安全领域参加OH的技术峰会和布道。                                                                               | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 测试     | 构建社区测试能力，让更多的社区开发者参与、贡献构建南北向生态兼容性测试标准和能力，看护南向设备和北向应用生态兼容性；<br>根据版本计划制定测试计划、规划测试活动，看护版本关键软件包质量；<br>参与制定、维护发布标准，参与管理发布过程，决策阻塞问题和关键缺陷的修复计划；<br>运作社区众测活动。                                                                                | 技术领域孵化流程；<br>技术领域决策流程。                                                |
| 图形图像   | 图形图像特性技术领域的竞争分析和关键技术识别，功能分解分配，模块间接口定义与维护管理，对应领域特性代码开发维护等；<br>负责图形图像技术领域系统设计方案的技术评审，技术决策，模块关键技术问题解决；<br>负责图形图像性技术领域的社区需求技术规划和梳理对应领域的共建需求梳理；<br>代表图形图像技术领域参加OH的技术峰会和布道。                                                               | 技术领域孵化流程；<br>技术领域决策流程。                                                |



## OpenHarmony PMC成员列表
| 姓名 | 账号   | 角色 | 领域 |
| :----: | :----: | :----: | :----: |
| 任革林 | [@im-off-this-week](https://gitee.com/im-off-this-week) |PMC主席 | 总架构 |
| 董金光 |[@dongjinguang](https://gitee.com/dongjinguang) | PMC成员 | 系统架构 |
| 万承臻 | [@wanchengzhen](https://gitee.com/wanchengzhen) | PMC成员 | 架构SIG |
| 付天福 | [@futianfu](https://gitee.com/futianfu) | PMC成员 |	安全架构 |
| 吴勇辉 | [@davidwulanxi](https://gitee.com/davidwulanxi) | PMC成员 | 版本发布SIG |
| 强波 | [@huawei_qiangbo](https://gitee.com/huawei_qiangbo) | PMC成员 | 应用框架SIG |
| 鲜余强 | [@klooer](https://gitee.com/klooer) | PMC成员 | 编译运行时SIG |
| 余枝强 | [@yuzhiqiang101](https://gitee.com/yuzhiqiang101) | PMC成员 | ArkUI框架SIG |
| 易见 | [@easy-to-see](https://gitee.com/easy-to-see) | PMC成员 | 内核SIG |
| 马耀辉 | [@stesen](https://gitee.com/stesen) | PMC成员 | 基础软件服务SIG |
| 赵文华 | [@shidi_snow](https://gitee.com/shidi_snow) | PMC成员 | 驱动框架SIG |
| 丁勇 | [@ding-yong](https://gitee.com/ding-yong) | PMC成员 | 社区产品规划 |
| 邢文华 | [@xhuazi](https://gitee.com/xhuazi) | PMC成员 | QA-SIG |
| 高涵一 | [@gaohanyi1982](https://gitee.com/gaohanyi1982) | PMC成员 | 测试SIG |
| 王意明 | [@youthdragon](https://gitee.com/youthdragon) | PMC成员 | 基础设施SIG |
| 张小田 | [@handyohos](https://gitee.com/handyohos) | PMC成员 | 基础软件服务SIG |
| 李煜 | [@abbuu](https://gitee.com/abbuu) | PMC成员 | 图形SIG |
| 巴延兴 | [@bayanxing](https://gitee.com/bayanxing) | PMC成员 | 测试SIG |


## PMC会议链接
- 会议时间: 每双周周四 9:30-11:00
- 议题申报: [OpenHarmony PMC Meeting Proposal](https://docs.qingque.cn/s/home/eZQB8yRFQfEFeAxk_6JKZEE0q?identityId=1tbICPd8j3s)
- 会议主题: 通过邮件通知
- 会议通知: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接

## 联系方式

| 地址                                 | 简介        | 用途说明                                                         |
| ---------------------------------------|---------- | ------------------------------------------------------------ |
| dev@openharmony.io  <img width=120/>| 开发邮件列表 <img width=100/> | OpenHarmony社区开发讨论邮件列表，任何社区开发相关话题都可以在邮件列表讨论。任何开发者可[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)。<img width=200/>|
| cicd@openharmony.io <img width=120/> | CI邮件列表  <img width=100/>| OpenHarmony CICD构建邮件列表，任何开发者可[订阅](https://lists.openatom.io/postorius/lists/cicd.openharmony.io)。<img width=200/>|
| pmc@openharmony.io  <img width=120/>| PMC邮件列表  <img width=100/>| PMC讨论邮件列表，PMC成员可[订阅](https://lists.openatom.io/postorius/lists/pmc.openharmony.io/)。<img width=200/>|

