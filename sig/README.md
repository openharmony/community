# OpenHarmony SIG 管理制度与操作指南
简体中文 | [English](./README_EN.md)

本文档详细介绍了 OpenHarmony 社区的 SIG（Special Interest Group）管理制度和操作指南，旨在为社区成员提供清晰、全面的 SIG 相关信息，包括 SIG 的申请、运营、变更、终止，以及仓库管理等。

## 一、SIG 概述

SIG 是 OpenHarmony 社区中由特定领域专家和爱好者组成的兴趣小组，旨在推动 OpenHarmony 在特定技术方向的发展。每个 SIG 拥有明确的技术方向和工作目标，并通过社区协作的方式进行项目开发和维护。

## 二、申请新 SIG

### 1. 准备申请

在申请新 SIG 之前，申请人需要：

*   **阅读 SIG 管理制度**：深入了解 OpenHarmony 社区 SIG 的运作规则，包括但不限于：
    *   **SIG 的定义与目标**：理解 SIG 在 OpenHarmony 社区中的角色和作用，以及 SIG 旨在解决的问题和实现的目标。
    *   **SIG 的组织架构**：了解 SIG 的成员角色（如 SIG Leader、Committer 等）、职责和权限。
    *   **SIG 的生命周期**：熟悉 SIG 从创建、运营、变更到终止的整个流程。
    *   **SIG 的决策机制**：了解 SIG 内部如何进行决策，如投票机制、共识机制等。
    *   **SIG 与 PMC 的关系**：明确 SIG 如何向 PMC 汇报工作，以及如何与 PMC 协同工作。
    *   **SIG 的沟通与协作方式**：了解 SIG 成员之间如何进行有效的沟通和协作，如邮件列表、例会、代码审查等。
    *   **SIG 的行为准则**：遵守 OpenHarmony 社区的行为准则，维护良好的社区氛围。
    *   可以通过仔细阅读本文档其他章节内容，来了解SIG的运作规则。
*   **确认技术方向的唯一性和可行性**：
    *   确保所申请的技术方向在 OpenHarmony 社区中尚未存在。
    *   查阅[已有的 SIG 列表](https://gitee.com/openharmony/community/tree/master/sig)和[历史 DEV 邮件列表](https://lists.openatom.io/hyperkitty/list/dev@openharmony.io/)。
    *   确认所申请的技术项目能够最终转化为 OpenHarmony 的新增部件和子项目。
    *   如有疑问，可通过邮件列表 [dev@openharmony.io](mailto:dev@openharmony.io) 咨询 PMC。
*   **准备 SIG 相关文档**：参考[SIG 申请模板](../meeting-notes/docs/openharmony_sig_template.pptx)，准备 SIG 章程等文档。
*   **梳理SIG组工作目标和范围**：明确 SIG 的工作目标、范围和预期成果。

### 2. 提交申请

*   **创建 SIG 提案初稿**：按照 [SIG 申请模板](../meeting-notes/docs/openharmony_sig_template.pptx) 撰写提案。
*   **提交 SIG 申请议题**：将[申请议题](https://shimo.im/sheets/16q8xyRaR9creOq7/MODOC)提交给 OpenHarmony 社区的 PMC，发起 SIG 成立申请。

### 3. PMC 审批提案

*   SIG 发起人在 PMC 例行会议上介绍待新建的 SIG，阐述 SIG 的目标、意义和计划。
*   PMC 对 SIG 的成立进行审批，包括技术方向、可行性、与现有 SIG 的关系等方面的评估，并决定是否批准 SIG 的成立以及相关 SIG 仓库和沟通渠道的建立。
*   评审会议形成会议纪要，记录 PMC 的审批意见。在创建SIG组时需附上该会议纪要。

### 4. 创建 SIG 组

PMC 审批通过后，SIG 发起人执行以下操作：

*   **Fork 代码库**：将 OpenHarmony 社区的代码库 Fork 到自己的个人仓下。
*   **创建 SIG 文件夹**：在 `sig` 目录下创建自己的 SIG 文件夹。
*   **拷贝 SIG 模板**：将 SIG 申请模板（`sig_template`）拷贝到该文件夹下。
*   **填写 SIG 信息**：根据实际情况填写 SIG 信息，可参考已有 SIG 的描述。
    ```
    git clone https://gitee.com/YOURGITEE/community
    cd ./community/sig
    cp -r sig_template sig_YOURSIGNAME
    cd sig_YOURSIGNAME
    mv sig_template_cn.md sig_YOURSIGNAME_cn.md
    mv sig_template.md sig_YOURSIGNAME.md
    vim sig_YOURSIGNAME_cn.md
    vim sig_YOURSIGNAME.md
    ```
*   **配置 SIG 组织信息**：编辑 `sig/sigs_list.toml` 文件，配置 SIG 组织信息。

## 三、SIG 运营

### 1. SIG 仓库及沟通渠道

*   SIG 使用 OpenHarmony 社区的统一基础设施（Gitee 仓库和邮件列表）进行工作和交流。
*   仓库创建、更名、退出的流程，请参考本文档“**仓库管理**”章节。
*   SIG 邮件列表创建：联系 **[xzmu@openatom.org](mailto:xzmu@openatom.org)** 并附上 SIG 审核通过的会议纪要，提供邮件列表名称和管理员邮箱（一般为 SIG 负责人）。
*   SIG 负责人应确保 SIG 仓库和沟通渠道的有效运作，并及时响应社区成员的反馈。

### 2. SIG 会议

*   SIG 应定期召开公开会议（线上或线下），保持 SIG 成员之间的信息同步和协作。
*   召集人应提前通知成员会议时间、地点和议程，确保会议的有效进行。
*   会议议程应包括进展报告、议题讨论和决策等，涵盖 SIG 工作的各个方面。
*   会议纪要应记录要点、讨论结果和决策事项，并及时分享和发布到对应的邮件列表（没有独立邮件列表的，可以复用 DEV 邮件列表），保持信息透明。

### 3. SIG 管理

*   SIG 负责人负责 SIG 的正常运行和管理，并与 PMC 保持沟通和协作。
*   负责人决定 SIG 的工作方向、任务分配和成员加入等事项，确保 SIG 目标的达成。
*   负责人定期向 PMC 和社区成员报告 SIG 工作进展和成果，保持信息公开透明。
*   负责人可根据需要组织工作小组或任务组，协调成员工作，推进项目进展。
*   如有需要，负责人可向 PMC 提出变更或终止 SIG 的申请，并提供充分的理由。
*   SIG 组需要定期召开例会，讨论和总结 SIG 组领域工作，并向 OpenHarmony PMC 组织进行定期汇报。如果 SIG 组中的 Leader 角色有变动，需要及时知会 OpenHarmony 社区 PMC 成员，并对组织信息和仓库权限进行相应的调整。

## 四、SIG 变更和终止

*   **SIG 变更**：包括负责人更替、工作方向调整、任务重新分配等。变更需通知 PMC 和 SIG 成员，并经过充分协商和讨论后确定。
*   **SIG 终止**：负责人向 PMC 提交终止申请，并提供充分的理由和解释。PMC 将对终止申请进行评估，并最终决定 SIG 的终止事宜。

## 五、仓库管理

### 1. OpenHarmony 项目仓库管理流程

OpenHarmony 项目从开源建仓到孵化准出进入主线，需要经历以下步骤：

1.  **申报架构 SIG 新建仓库申请的议题**：提交新建仓库的申请。
2.  **申报架构 SIG 孵化准出预审的议题**：进行孵化准出的预审。
3.  **申报 QA SIG 孵化准出终审的议题**：完成孵化准出的终审，并解决所有遗留问题。

**注意事项**：

*   **孵化准出条件**：满足基本合规要求，完成孵化仓目标准出的关联仓的联合构建。
*   **代码交叉检视**：新建仓库必须配置至少 2 名及以上的 Committer 以支持代码交叉检视功能。

### 2. SIG 组仓库新增、退休、更名申请

1.  **申请架构 SIG 评审**：
    *   新增、退休、更名：参考[模板1--新增、退休、更名](../sig/sig_architecture/meetings/repository_review_template.pptx)。
    *   开源软件引入：参考[模板2--开源软件引入](../sig/sig_architecture/meetings/OpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx)。
    *   申请[架构SIG](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC)议题评审。
2.  **新增仓电子流申请**：架构 SIG 评审通过后，参考[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” --> "SIG管理" --> “SIG仓申请”。
3.  **仓库退休、更名电子流申请**：架构 SIG 评审通过后，参考[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” --> "SIG管理" --> “仓管理”。

### 3. 仓库孵化准出

1.  **申请架构 SIG 孵化预审**：[申请议题](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC)，参考[模板](../sig/sig_architecture/meetings/repository_review_template.pptx)。
2.  **申请质量 SIG 孵化准出评审**：[申请议题](https://shimo.im/sheets/AQrrKb4pJCUFYkHR/MODOC)，参考[准出标准](../sig/sig_qa/guidance_for_incubation_project_graduation_cn.md)。
3.  **提交仓库孵化准出电子流**：质量 SIG 准出评审通过后，提交[孵化准出电子流](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” --> "SIG管理" --> “孵化报告”。