#                                          OpenHarmony社区代码仓管理规定


| **文件名称**             | **版本** | **拟制/修订日期** | **拟   制** | **批准** |
| -------------------- | ------ | ----------- | --------- | ------ |
| OpenHarmony社区代码仓管理规定 | V1.0   | 2022-6-30   | QA   Sig  | PMC    |

## 1 目的

为规范OpenHarmony社区代码仓操作要求，指导社区角色进行规范化操作，确保社区的代码稳定且有质量的发展，达成可信开源社区要求，制定OpenHarmony社区代码仓管理规定。

## 2 适用范围

- **社区角色：包括Contributor、Committer、SIG Leader、PMC，角色定义见：**

<https://www.openharmony.cn/role> ，成员名单可通过以下查询。 

| **社区角色** | 描述                                                         | **成员名单**                                                 |
| ------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| PMC          | 项目管理委员会（PMC）成员，拥有代码库写权限、OpenHarmony 新版本发布、Roadmap发布、新PMC/Committer等社区事务的投票权、以及新的 PMC 成员和 Committer 提名权。PMC负责OpenHarmony 社区的管理工作，包括开源OpenHarmony 社区版本规划、竞争力规划、特性开发代码维护、资料开发、补丁规划等；组织PMC委员的选举和退出，负责Committer的任命和退出；负责OpenHarmony 社区SIG的申请准入、SIG孵化项目指导、SIG毕业项目准入等SIG生命周期管理等。 | https://gitee.com/openharmony/community/blob/master/zh/pmc.md |
| Committer    | Committer拥有SIG子领域的代码仓写权限。Committer 负责SIG领域软件模块设计与评审，负责代码审核及维护，处理OpenHarmony社区的issue、邮件列表问题，辅导Contributors快速理解SIG领域架构设计并提升代码开发技能。 | https://gitee.com/openharmony/community/blob/master/sig/sigs_list.toml |
| Contributor  | 有一定代码编程经验的开发者。Contributors以参与OpenHarmony 社区代码贡献、文档贡献、技术方案讨论及设计、解答用户问题、发表技术文章及视频课程、组织策划开源OpenHarmony 社区活动等形式参与OpenHarmony 社区。 | -                                                            |
| Sig Leader   | SIG Leader负责特定SIG的运营及维护。SIG Leader负责定义特定SIG的工作范围及业务目标，并负责对应SIG的运营及维护；吸纳并发展Committer参与对应SIG的项目孵化、文档完善及社区推广；定期在PMC项目管理委员会汇报SIG孵化项目及SIG运营进展，并基于PMC的指导建议完成相关改进。 | https://gitee.com/openharmony/community/blob/master/sig/sigs_list.toml |

- **OpenHarmony Gitee 企业账号IT系统角色** 


| **系统角色** | **角色定义**                                 | **成员名单**                    |
| -------- | ---------------------------------------- | --------------------------- |
| IT 系统管理员 | OpenHarmony的Gitee系统管理员，负责配置IT 系统操作员      | 基础设施工作组 组长 1名   基金会派驻代表 1 名 |
| IT 系统操作员 | OpenHarmony的Gitee系统操作员，负责根据业务决策进行IT系统操作实施 | 由基础设施工作组 组长任命               |

*注：为确保IT管理与IT实施人员分离，同一人不能同时担任IT系统管理员和IT系统操作员。*

## 3 代码仓说明

OpenHarmony代码仓包含：OpenHarmony主仓、OpenHarmony-SIG仓、 OpenHarmony-TPC仓；各仓定义如下：

- OpenHarmony主仓：指 https://gitee.com/openharmony 下的所有代码仓库，存放满足成熟度要求的OpenHarmony项目代码。 

- OpenHarmony-SIG仓：指 https://gitee.com/openharmony-sig 下的所有代码仓库，存放OpenHarmony SIG孵化子项目的代码；在孵化成功后，会根据代码类别进入到OpenHarmony主仓或者是OpenHarmony-TPC仓。 

- OpenHarmony-TPC仓：指 https://gitee.com/openharmony-tpc 下的所有代码仓库，存放满足成熟度要求的OpenHarmony三方库子项目代码。



## 4 代码仓的管理要求

为规范社区代码仓操作，降低风险，任何对代码仓库的操作都要求遵循“先进行业务决策，再进行IT实施”的原则进行，业务决策与IT实施分离；禁止任何未经过决策的IT实施。 

下表规定了针对代码仓不同场景下的决策组织/角色及实施组织/角色

- 所有代码仓操作的决策组织为PMC 

- 部分操作场景已由PMC授权到对应的组织/角色 

- 如存在表中未覆盖的代码仓操作场景，缺省决策组织为PMC 

- 所有代码仓操作的IT实施组织为IT系统操作员 


|        | 操作类型    | 操作         | 描述                                       | 决策组织/角色 | 被授权决策组织/角色（如有授权） | 实施组织/角色 |
| ------ | ------- | ---------- | ---------------------------------------- | ------- | ---------------- | ------- |
| 代码仓库操作 | 新建      | 新建         | 创建代码仓，从无到有                               | PMC     | 架构SIG            | IT系统操作员 |
| 代码仓库操作 | 迁移      | 迁移         | sig孵化、代码仓归档涉及的迁移                         | PMC     | 架构SIG            | IT系统操作员 |
| 代码仓库操作 | 废弃      | 废弃         | 因为业务变化,仓库不再使用, 修改状态为暂停/停止                | PMC     | 架构SIG            | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 修改仓库描述     |                                          | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 设置安全风险标识   | 设置后允许提交安全issue, 仅允许企业成员+仓库成员查看           | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 是否允许在线编辑   |                                          | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 设置禁止强制push | 保护库上代码不被误操作覆盖导致丢失历史记录                    | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 分支保护规则设置   | 防止分支被误操作删除/强制推送                          | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库属性配置  | 推送规则设置     | 限制单个文件大小                                 | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库人员管理  | 代码审查设置     | 给committer添加审查权限, 给门禁账号添加测试权限            | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 仓库人员管理  | 仓库管理员维护    | 将committer添加到仓库,设置为管理员角色; 非committer从仓库删除 | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 版本分支管理  | 新建分支/标签    | 按PMC版本规划从指定节点新建分支,从指定分支新建标签              | PMC     | Release SIG      | IT系统操作员 |
| 代码仓库操作 | 例外合入操作类 | 三方软件版本升级   | 三方软件的版本升级往往携带上游社区提交，因而导致DCO检查失败,在确认合入PR失败仅由DCO失败引起并且不存在法务合规问题的情况下，需要例外合入PR | PMC     | 不授权              | IT系统操作员 |
| 代码仓库操作 | 例外合入操作类 | 紧急情况回退PR   | 由于合入PR导致的编译问题，经过PR提交人/Committer+IT系统操作员共同确认后, 需要例外回退PR | PMC     | Committer        | IT系统操作员 |
| 代码仓库操作 | 例外合入操作类 | 其它情况       | 其它紧急情况的例外合入                              | PMC     | 不授权              | IT系统操作员 |



## 5 审视

- 每个季度由IT 系统操作员输出 代码仓操作 及 人员的权限配置 的变更报告，送递 IT系统管理员和 QA Sig Leader。 

- IT系统管理员 和 QA Sig Leader 负责审查变更报告，确保及时发现异常或违规操作，在PMC例会上进行通报并制定改进措施。 


## 6 变更记录

本规定由QA Sig制定并在2022年6月30日 PMC会议上汇报通过。 

规定的变更需由QA Sig制定，并报PMC例会批准通过。 