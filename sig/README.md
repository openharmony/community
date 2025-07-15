# OpenHarmony SIG 管理制度与操作指南

简体中文 | [English](./README_EN.md)

本文档旨在为 OpenHarmony 社区成员提供清晰、全面的 SIG（Special Interest Group）管理制度与操作指南。文档首先阐述 SIG 的核心治理框架，包括其组织架构、生命周期与决策机制；随后提供详细的操作指南，覆盖 SIG 的申请、日常运作、变更、终止及仓库管理等流程。

## 一、SIG 概述

SIG（Special Interest Group）是 OpenHarmony 社区中，由对特定技术领域充满热情的专家和贡献者组成的兴趣小组。每个 SIG 聚焦于一个明确的技术方向，设定清晰的工作目标，通过开放、透明的社区协作方式，推动 OpenHarmony 在该领域的技术演进、项目开发与生态维护。

为鼓励更广泛的生态协作并明确社区治理边界，SIG 所孵化或管理的项目不强制要求捐赠给 OpenHarmony 项目群或开放原子开源基金会，所有向 SIG 所辖仓库贡献代码的个人或实体，均须按照OpenHarmony项目群要求签署代码贡献协议。

## 二、SIG 治理

本章节定义了 OpenHarmony SIG 的治理框架，是所有 SIG 必须遵守的核心准则，确保其健康、有序、高效地运作。

### 1. SIG 组织架构与角色职责

每个 SIG 均包含以下核心角色：

- **SIG Leader(s)**：SIG 的负责人，通常由 1-2 名在该领域有深入见解和影响力的专家担任。
  - **职责**：
    - 负责制定和推动 SIG 的技术愿景、目标和路线图。
    - 召集和主持 SIG 例会，引导技术讨论和决策。
    - 代表 SIG 与 PMC (项目管理委员会) 及其他 SIG 进行沟通协调。
    - 定期向 PMC 和社区汇报 SIG 的工作进展、成果与风险。
    - 维护 SIG 的健康运作，激励和发展社区成员。
    - 负责 SIG 仓库权限和邮件列表等基础设置的管理。
- **Committer**：SIG 的核心贡献者，在特定代码仓库拥有写权限。
  - **职责**：
    - 深度参与 SIG 的技术方案设计和讨论。
    - 高质量地完成代码开发、提交和维护工作。
    - 积极参与代码审核（Code Review），保障代码质量。
    - 指导和帮助新成员融入 SIG。
- **Member**：所有对 SIG 所属领域感兴趣并参与贡献的社区成员。
  - **职责**：
    - 参与 SIG 的公开会议和邮件列表讨论。
    - 通过提交 Issue，Pull Request 等方式为 SIG 做出贡献。
    - 遵守 OpenHarmony 社区行为准则，共同维护良好的社区氛围。

### 2. SIG 生命周期

SIG 的生命周期包括创建申请、运作、变更和终止四个阶段。

- **创建 (Creation)**
  SIG 的创建需经过严格的审批流程，以确保其技术方向符合 OpenHarmony 的整体发展战略，且具备可行性和独特性。申请人需准备充分的材料，通过 PMC 评审后方可成立。详细流程请参见运作指南部分。
- **运作 (Operation)**
  SIG 批准成立后，即进入其生命周期中的核心活动阶段。在此阶段，SIG 遵循其治理章程，通过例会、代码贡献、技术讨论等方式积极开展工作，以实现其既定目标。SIG 的健康状况，如活跃度、贡献产出和社区影响力，将受到持续关注。所有日常运作活动应遵循本指南第三章《SIG 运作指南》的详细流程。
- **变更 (Changes)**
  当 SIG 的工作范围、目标或 Leader 发生重大变化时，需要向 PMC 报备或申请审批。
  - **Leader 变更**：需及时知会 PMC，并更新 SIG 组织信息和相关权限。
  - **范围调整**：需与相关 SIG 充分沟通，并通过 PMC 评审，确保职责清晰，避免技术领域重叠。
- **终止 (Termination)**
  当 SIG 完成其历史使命、长期不活跃或其技术方向不再符合社区发展需求时，可以被终止。
  - SIG Leader 可向 PMC 主动提交终止申请，并说明理由。
  - PMC 也有权根据 SIG 的活跃度和贡献度，决定是否终止某个 SIG。
  - 终止后，其SIG组织或归属的代码仓库将按流程进行退休处理。

### 3. 决策机制与沟通

- **决策机制**：SIG 内部决策遵循“共识优先”原则。对于重要技术决策，应通过公开会议和邮件列表充分讨论，力求达成共识。若无法达成共识，则由 SIG Leader(s) 根据讨论情况做出决策，或申请架构SIG/PMC组织进行最终决策。
- **沟通透明**：所有 SIG 的工作都应在公开渠道进行。
  - **例会**：定期召开公开会议，会议议程提前公布，会议纪要及时发布至邮件列表。
  - **邮件列表**：作为官方沟通渠道，用于发布通知、讨论议题和归档决策。无独立邮件列表的 SIG 可使用 [dev@openharmony.io](dev@openharmony.io)。
  - **向 PMC 汇报**：SIG Leader需定期向 PMC 汇报工作进展，接受社区监督和指导。

## 三、SIG 运作指南

本章节提供了执行 SIG 治理规则的具体操作流程和方法。

### 1. 申请新 SIG

#### 1.1 准备申请

在申请新 SIG 之前，申请人需要：

- **阅读 SIG 管理制度**：深入理解本文档，特别是“SIG 治理”章节，明确 SIG 的运作规则、角色职责和生命周期。
- **确认技术方向的唯一性和可行性**：
  - 查阅[已有的 SIG 列表](https://gitee.com/openharmony/community/tree/master/sig)和[历史 DEV 邮件列表](https://lists.openatom.io/hyperkitty/list/dev@openharmony.io/)，确保所申请的技术方向在社区中尚不存在。
  - 确认所申请的技术项目能够最终转化为 OpenHarmony 的新增部件和子项目。
  - 如有疑问，可通过邮件列表 [dev@openharmony.io](mailto:dev@openharmony.io)咨询 PMC。
- **准备 SIG 章程与目标**：参考[SIG 申请模板](../meeting-notes/docs/openharmony_sig_template.pptx)，准备 SIG 章程，并清晰地梳理 SIG 的工作目标、范围和预期成果。

#### 1.2 提交申请

- **创建 SIG 提案初稿**：按照 [SIG 申请模板](../meeting-notes/docs/openharmony_sig_template.pptx) 撰写提案。
- **提交 SIG 申请议题**：将[申请议题](https://shimo.im/sheets/16q8xyRaR9creOq7/MODOC)提交给 OpenHarmony 社区的 PMC，发起 SIG 成立申请。

#### 1.3 PMC 审批提案

- SIG 发起人在 PMC 例行会议上介绍待新建的 SIG，阐述 SIG 的目标、意义和计划。
- PMC 对 SIG 的成立进行审批，评估其技术方向、可行性及与现有 SIG 的关系，并决定是否批准。
- 评审会议形成会议纪要，记录 PMC 的审批意见。该会议纪要是后续创建 SIG 的必要凭证。

#### 1.4 创建 SIG 组

PMC 审批通过后，SIG 发起人需在 openharmony/community 仓库中完成以下操作：

1. **Fork 并 Clone 代码库**：将 openharmony/community 库 Fork 到个人空间后 Clone 到本地。

2. **创建 SIG 文件夹**：在 sig 目录下创建以 SIG 名称命名的文件夹（如 sig_YOURSIGNAME）。

3. **创建 SIG 描述文件**：将 sig/sig_template 文件夹中的模板文件拷贝至新创建的 SIG 文件夹，并根据 SIG 实际情况重命名和填写内容。

   ```
   # 假设Fork 到个人空间后 Clone 到本地
   cd ./community/sig
   cp -r sig_template sig_YOURSIGNAME
   cd sig_YOURSIGNAME
   mv sig_template_cn.md sig_YOURSIGNAME_cn.md
   mv sig_template.md sig_YOURSIGNAME.md
   # 使用编辑器编辑 sig_YOURSIGNAME_cn.md 和 sig_YOURSIGNAME.md 文件
   ```

4. **配置 SIG 组织信息**：编辑 sig/sigs_list.toml 文件，添加新 SIG 的组织信息。

5. **提交 Pull Request**：将上述修改提交一个 PR 到 openharmony/community 仓库，PR 中需附上 PMC 审批通过的会议纪要链接。

### 2. 日常运作

- **沟通渠道建立与管理**：
  - **仓库**：SIG 使用 OpenHarmony 社区的 Gitee/Gitcode 仓库进行代码托管。仓库的创建、更名、退休流程见下文“仓库管理”章节。
  - **邮件列表**：无独立邮件列表的 SIG 可复用 [dev@openharmony.io](dev@openharmony.io)；如果希望创建独立邮件列表，可联系 **[xzmu@openatom.org](mailto:xzmu@openatom.org)** 申请创建 SIG 专属邮件列表，需附上 SIG 审核通过的会议纪要，并提供列表名称和管理员邮箱（通常为 SIG Leader）。
- **SIG 会议**：
  - **频率**：SIG 应定期召开公开会议（线上或线下），保持信息同步和协作。
  - **通知**：召集人应提前通过邮件列表等方式通知会议时间、地点和议程。
  - **纪要**：会后应及时整理会议纪要，记录要点、讨论结果和决策事项，并发布到邮件列表，定期归档到community/sig_YOURSIGNAME/meetings。
- **SIG 管理与汇报**：
  - SIG Leader 负责 SIG 的日常管理，包括工作方向把控、任务分配等。
  - SIG 需定期向 PMC 和社区汇报工作进展与成果，保持信息公开透明。
  - 若 SIG Leader 发生变动，需及时通知 PMC，并更新组织信息和仓库权限。

### 3. 仓库管理

#### 3.1 OpenHarmony 项目仓库孵化流程

OpenHarmony 项目从开源建仓到孵化成熟并进入主干，通常需经历以下阶段：

1. **新建仓库申请**：向架构 SIG 提交新建仓库申请议题。
2. **孵化准出预审**：向架构 SIG 提交孵化准出预审议题。
3. **孵化准出终审**：向 QA SIG 提交孵化准出终审议题，解决所有遗留问题后完成准出。

**注意**：新建仓库必须配置至少 2 名 Committer 以支持代码交叉检视（cross review）；满足基本合规要求，完成孵化仓目标准出的关联仓的联合构建。

#### 3.2 仓库新增、退休、更名申请

1. **申请架构 SIG 评审**：
   - 新增、退休、更名：参考[模板1--新增、退休、更名](../sig/sig_architecture/meetings/repository_review_template.pptx)。
   - 开源软件引入：参考[模板2--开源软件引入](../sig/sig_architecture/meetings/OpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx)。
   - 提交[架构 SIG](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC) 议题进行评审。
2. **提交电子流申请**：架构 SIG 评审通过后，根据需求提交电子流。
   - **新增仓**：参考[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” -> "SIG管理" -> “SIG仓申请”。
   - **仓库退休/更名**：参考[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” -> "SIG管理" -> “仓管理”。

#### 3.3 仓库孵化准出

1. **申请架构 SIG 孵化预审**：提交[议题](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC)，参考[模板](../sig/sig_architecture/meetings/repository_review_template.pptx)。
2. **申请质量 SIG 孵化准出评审**：提交[议题](https://shimo.im/sheets/AQrrKb4pJCUFYkHR/MODOC)，参考[准出标准](../sig/sig_qa/guidance_for_incubation_project_graduation_cn.md)。
3. **提交仓库孵化准出电子流**：质量 SIG 准出评审通过后，在[此平台](http://ci.openharmony.cn/workbench/ciCommunity)提交：“操作指南” -> "SIG管理" -> “孵化报告”。