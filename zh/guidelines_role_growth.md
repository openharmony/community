# **OpenHarmony社区角色定义及晋升机制**

## 1. 角色定义

- 1.1 用户 (Users)  ：使用OpenHarmony项目的广大用户，以Issue形式向OpenHarmony 社区反馈问题和功能建议。

- 1.2 贡献者 (Contributors)  ：有一定代码编程经验的开发者。Contributors以参与OpenHarmony 社区代码贡献、文档贡献、技术方案讨论及设计、解答用户问题、发表技术文章及视频课程、组织策划开源OpenHarmony 社区活动等形式参与OpenHarmony 社区。

- 1.3 提交者 (Committers) ： Committer拥有SIG子领域的代码仓写权限。Committer 负责SIG领域软件模块设计与评审，负责代码审核及维护，处理OpenHarmony社区的issue、邮件列表问题，辅导Contributors快速理解SIG领域架构设计并提升代码开发技能。

- 1.4 SIG 负责人（SIG Leader）： SIG Leader负责特定SIG的运营及维护。SIG Leader负责定义特定SIG的工作范围及业务目标，并负责对应SIG的运营及维护；吸纳并发展Committer参与对应SIG的项目孵化、文档完善及社区推广；定期在PMC项目管理委员会汇报SIG孵化项目及SIG运营进展，并基于PMC的指导建议完成相关改进。

- 1.5 PMC 成员 (PMC)  ：项目管理委员会（PMC）成员，拥有代码库写权限、OpenHarmony 新版本发布、Roadmap发布、新PMC/Committer等社区事务的投票权、以及新的 PMC 成员和 Committer 提名权。PMC负责OpenHarmony 社区的管理工作，包括开源OpenHarmony 社区版本规划、竞争力规划、特性开发代码维护、资料开发、补丁规划等；组织PMC委员的选举和退出，负责Committer的任命和退出；负责OpenHarmony 社区SIG的申请准入、SIG孵化项目指导、SIG毕业项目准入等SIG生命周期管理等。

## 2. 晋升标准和流程

### 2.1 晋升标准简介 :

- 2.1.1 如何晋升Committer: 优秀的OpenHarmony 社区贡献者，经现任PMC/Committer提名和投票后，可以成为OpenHarmony 社区Committer，Committer按照权限可分为Approver审批人和Reviewer审阅人。
    - Approver审批人 :
        - 1. OpenHarmony项目贡献至少3个月
        - 2. 至少10个PR的主要审阅人
        - 3. 至少有30个PR的审核意见或30个实质性的代码PR提交
        - 4. 对所申请的仓库代码非常熟悉
        - 5. 由对应仓库的审批人或SIG Leader或PMC提名
    - Reviewer审阅人 :
        - 1. OpenHarmony项目贡献至少2个月
        - 2. 至少有5个PR的主要审阅人
        - 3. 至少有10个PR的审核意见或10个实质性的代码PR提交
        - 4. 对所申请的仓库代码非常熟悉
        - 5. 可以由对应仓库的审批人或审阅人提名

- 2.1.2 如何成为SIG Leader: 优秀的OpenHarmony Committer，通过PMC项目管理委员会批准后，可以成为对应的SIG的SIG Leader。
  - 新申请SIG的SIG Leader： 任何开发者可以在社区中寻找2-3个有共同兴趣及目标的开发者，确定SIG Leader候选人，通过PMC项目管理委员会发送新建SIG的PR申请，经PMC项目管理委员会批准后，可以成为此新SIG的SIG Leader
  - 已有SIG的SIG Leader： 已经是对应SIG所看护领域的仓库Committer，可以由对应SIG的Committer、SIG Leader或PMC成员提名

- 2.1.3  如何晋升PMC：优秀的OpenHarmony 社区Committer，经现任PMC成员提议和投票后，可以成为OpenHarmony 社区PMC。

### 2.2 晋升Committer投票流程 :

- 2.2.1  由现任PMC/Committer提名，以标题“[VOTE] New Committer [Approver/Reviewer] xxx ”发送邮件至[pmc@openharmony.io](mailto:pmc@openharmony.io)。

- 2.2.2 所有PMC成员有权通过“+1”或“-1”形式表示支持或反对，PMC通过回复邮件发送投票结果，投票时间一般持续72个小时。

- 2.2.3 提名Approver权利的Committer获得四票及以上赞成票，无反对票情况下投票通过。投反对票的PMC成员必须说明反对的具体问题（无问题描述的反对票无效），投票发起人可针对具体问题进行澄清或修复。

- 2.2.4 提名Reviewer权利的Committer获得三票及以上赞成票，无反对票情况下投票通过。投反对票的PMC成员必须说明反对的具体问题（无问题描述的反对票无效），投票发起人可针对具体问题进行澄清或修复。

- 2.2.5 投票通过后，PMC主席在OpenHarmony社区公告新Committer。

### 2.3  晋升PMC投票流程 :

- 2.3.1 由现任PMC提名，并在PMC会议上进行投票决策；

- 2.2.2 被提名的PMC候选人，在获得2/3及以上的参会PMC成员赞成下投票通过。有投票权的到会PMC成员超过应到会PMC成员的一半，会议方为有效。

- 2.2.3 投票通过后，PMC主席在OpenHarmony社区公告新PMC。

## 3. 非活跃成员退出标准和流程

### 3.1 非活跃成员定义 :

- 3.1.1 非活跃Committer: 连续6个月以上没有在OpenHarmony 社区参与代码审核、PR提交、设计评审等
- 3.1.2 非活跃SIG： 连续3个月以上未召开SIG小组会议，连续6个月以上没有在PMC项目管理委员会汇报SIG孵化项目及SIG运营进展
- 3.1.3 非活跃PMC成员： 连续3个月以上未参与PMC会议，连续6个月以上没有在OpenHarmony 社区参与代码审核、PR提交、设计评审、社区活动推广等

### 3.2 非活跃成员退出流程 :

- 3.2.1 非活跃成员退出有两种方式：

    - 方式一:
        - 1. PMC主席自己或委托PMC成员审视并收集非活跃成员名单；
        - 2. PMC会议不定期审视非活跃成员名单，并对不活跃成员进行退出投票，在获得2/3及以上的参会PMC成员赞成下投票通过。有投票权的到会PMC成员超过应到会PMC成员的一半，会议方为有效。
        - 3. PMC主席自己或委托PMC成员对投票通过的待退出不活跃成员进行退出处理。

    - 方式二:
        - 1. 非活跃成员自发邮件申请退出，邮件标题采用“Inactive [Committer/SIG Leader/PMC] xxx ” ，并发送邮件至[pmc@openharmony.io](mailto:pmc@openharmony.io)；
        - 2. PMC主席自己或委托PMC成员对申请退出的非活跃成员做退出处理。



