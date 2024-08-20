# **OpenHarmony社区角色定义及晋升机制**

## 1. 角色定义

- **1.1 用户 (Users)**: 使用OpenHarmony项目的广大用户，他们通过Issue向OpenHarmony社区反馈问题和提出功能建议。

- **1.2 贡献者 (Contributors)**: 拥有一定编程经验的开发者，他们通过代码贡献、文档贡献、技术方案讨论、问题解答、发表技术文章、策划社区活动等方式参与OpenHarmony社区。

- **1.3 提交者 (Committers)**: Committer拥有特定SIG子领域代码仓库的写权限，负责模块设计与评审、代码审核与维护，处理社区的Issue，帮助Contributors提升代码开发技能。Committer的申请是**按代码仓库维度**进行的，即每个Committer的权限和职责都与其所申请的特定代码仓库相关。

- **1.4 SIG 负责人（SIG Leader）**: 负责特定SIG的运营和维护，定义SIG的工作范围和目标，吸纳并发展Committer参与项目孵化和推广，定期向PMC汇报SIG运营进展，并基于PMC的指导建议完成相关改进。
- **1.5 PMC 成员 (PMC)**: 项目管理委员会（PMC）成员，拥有代码库写权限、OpenHarmony 新版本发布、Roadmap发布、新PMC/Committer等社区事务的投票权、以及新的 PMC 成员和 Committer 提名权。PMC负责OpenHarmony 社区的管理工作，包括开源OpenHarmony 社区版本规划、竞争力规划、特性开发代码维护、资料开发、补丁规划等；组织PMC委员的选举和退出，负责Committer的任命和退出；负责OpenHarmony 社区SIG的申请准入、SIG孵化项目指导、SIG毕业项目准入等SIG生命周期管理等。

## 2. 晋升标准和流程

### 2.1 晋升标准简介

- **2.1.1 如何晋升Committer**: 优秀的贡献者可以**按仓库维度**申请成为Committer。申请时需满足以下条件：
  1. 至少参与OpenHarmony项目贡献2个月。
  2. 对所申请的代码仓库提交至少5个PR的审核意见。
  3. 对所申请的代码仓库提交10个实质性的代码PR。
  4. 对所申请的代码仓库非常熟悉。
  5. 申请人需由对应代码仓库的审批人或审阅人提名。

- **2.1.2 如何成为SIG Leader**: 优秀的Committer通过PMC批准后，可成为SIG Leader。申请方式分为两种：
  - **新SIG的SIG Leader**: 任何开发者可以寻找3个及以上志同道合的开发者，确定SIG Leader候选人，通过PMC申请新建SIG，经批准后成为新SIG的SIG Leader。
  - **已有SIG的SIG Leader**: 已是对应SIG领域的Committer，可以由该SIG的Committer、SIG Leader或PMC成员提名。

- **2.1.3 如何晋升PMC**: 优秀的Committer可由现任PMC成员提议并投票后成为PMC成员。

### 2.2 晋升Committer投票流程

1. **提名与邮件通知**: 现任PMC或Committer提名申请人，并以标题“[VOTE] New Committer [Approver/Reviewer] xxx”发送邮件至[pmc@openharmony.io](mailto:pmc@openharmony.io)。

2. **PMC成员投票**: 所有PMC成员通过“+1”或“-1”的形式进行投票，投票时间一般为72小时。

3. **Approver投票通过条件**: 提名为Approver的Committer需要至少获得四票赞成且无反对票。反对票必须附有具体理由，否则视为无效。投票发起人可以对问题进行澄清或修复。

4. **Reviewer投票通过条件**: 提名为Reviewer的Committer需要至少获得三票赞成且无反对票。反对票同样需附有具体理由，否则视为无效。

5. **投票结果公告**: 投票通过后，PMC主席将在OpenHarmony社区公告新晋升的Committer。

6. **参考操作流程**: 实际操作流程可参考[更新Committer工作流程](./update_committer_workflow.md)。

### 2.3 晋升PMC投票流程

1. **提名与会议陈述**: 由现任PMC提名候选人，并在PMC会议上进行陈述。

2. **投票决策**: PMC成员进行投票，候选人需获得至少2/3的参会PMC成员的赞成票。会议有效的前提是有投票权的到会PMC成员超过应到会成员的一半。

3. **投票结果公告**: 投票通过后，PMC主席将在OpenHarmony社区公告新晋升的PMC成员。

## 3. 非活跃成员退出标准和流程

### 3.1 非活跃成员定义

- **3.1.1 非活跃Committer**: 连续6个月以上未参与代码审核、PR提交或设计评审等活动。
- **3.1.2 非活跃SIG**: 连续3个月以上未召开SIG会议，或连续6个月以上未在PMC汇报SIG项目进展。
- **3.1.3 非活跃PMC成员**: 连续3个月以上未参与PMC会议，或连续6个月以上未参与代码审核、PR提交、设计评审、社区活动推广等。

### 3.2 非活跃成员退出流程

- **3.2.1 非活跃成员退出方式**:
  - **方式一**:
    1. PMC主席或指定PMC成员收集非活跃成员名单。
    2. PMC会议审视非活跃成员名单，并进行退出投票。投票通过需获得2/3的参会PMC成员的赞成票。
    3. PMC主席或指定PMC成员对投票通过的非活跃成员进行退出处理。

  - **方式二**:
    1. 非活跃成员自行申请退出，邮件标题为“Inactive [Committer/SIG Leader/PMC] xxx”，发送至[pmc@openharmony.io](mailto:pmc@openharmony.io)。
    2. PMC主席或指定PMC成员对申请退出的非活跃成员进行处理。

