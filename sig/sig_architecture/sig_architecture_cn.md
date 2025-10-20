# sig_architechture

简体中文 | [English](./sig_architecture.md)

**说明**：本SIG的内容遵循OpenHarmony的PMC管理章程 [README](/zh/pmc.md)中描述的约定。

## SIG组工作目标和范围

### 工作目标

制定OpenHarmony架构设计原则，负责OpenHarmony架构的定义、设计、演进和看护，并建立清晰的架构评审及SIG孵化毕业流程与标准。

### 工作范围

- 负责OpenHarmony整体架构演进，以及新增、合并、拆分、移除子系统/部件/代码仓等架构变更的评审与决策。
- 负责修订和维护《架构设计原则》与《OpenHarmony 系统架构》等核心架构文档。
- 定义和看护SIG（或新特性、子系统）从孵化到毕业的架构验收标准，并组织相应的评审。
- 提供[新增三方开源软件选项评估模板](https://www.google.com/url?sa=E&q=meetings%2FOpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx)。

## SIG孵化毕业标准

为了确保 OpenHarmony 各技术方向的健康、可持续发展，架构 SIG 负责对新孵化的 SIG（或特性、子系统等）进行架构看护和验收。以下是 SIG 从孵化到毕业所需满足的基本架构验收标准：

| 验收标准 | 具体要求 |
| :--- | :--- |
| 支撑的业务 | <ul><li>业务有明确的用户需求或社区共识，具备通用性，能够服务于广泛场景，而非为特定客户或场景专属定制。 |
| 架构合理性 | <ul><li>分层清晰：架构设计符合社区的整体分层逻辑，在系统中的分层归属合理。</li><li>依赖明确：模块间的依赖关系清晰、合理，无循环依赖，避免不合理的跨层调用。</li><li>高内聚、低耦合：功能单元（模块/部件）划分合理，内部功能高度相关，模块间耦合度低，易于独立演进和维护。</li></ul> |
| 质量属性达标 | <ul><li>定义明确：对内存、ROM占用、性能、可靠性、可测试性、可维护性和可扩展性等关键质量属性有明确且合理的量化指标。</li><li>结果达成：已有测试数据或实践证明，各项质量属性指标已达成预设目标。</li></ul> |
| 功能完备度 | <ul><li>核心功能覆盖度：核心功能已全面实现，能够满足目标场景的基本需求。</li><li>场景适配广度：能够适配目标领域的主流应用场景。</li><li>扩展能力：提供必要的扩展机制（如插件、配置、API等），使得用户二次开发成本与业界主流方案相当，即可解决目标领域的绝大多数问题。</li></ul> |
| 技术成熟度 | <ul><li>关键技术方案已有成熟的实践支撑，已被多个外部用户或下游厂商集成和商用。</li><li>有明确的用户反馈、使用报告或商用案例，内容可包括使用效果、性能数据及改进建议等。</li></ul> |
| 文档完整性 | <ul><li>代码仓文档：各代码仓的 `README.md` 文件应包含功能简介、逻辑架构图、编译构建说明以及与其它仓的交互关系。</li><li>用户文档：提供完善的开发者使用指南、API参考手册（如涉及）和典型场景的示例代码（Sample/Codelab）。</li><li>质量要求：文档结构清晰，内容准确全面，示例可运行，能够有效指导开发者快速上手使用。</li></ul> |
| 系统兼容性 | <ul><li> 对开发者可见的特性（如API、二进制接口、文件格式等），需在兼容性规范文档中有明确的说明，并在系统能力（syscaps）中有具体的定义，确保系统升级和应用开发的兼容性。 |
| API设计合理性 | <ul><li> 对于提供API的代码仓，其API设计需遵循社区统一规范，并获得 API SIG 的正式评估与认可。 |

## SIG组成员

### Leader

- @im-off-this-week([https://gitcode.com/im-off-this-week](https://gitcode.com/im-off-this-week))

### 会议

- **会议时间**：每周二 9:30
- **会议申报**：[OpenHarmony SIG-Architecture Meeting Proposal](https://shimo.im/sheets/StzhuFkEk38enrnl/MODO)
- **会议链接**: Welink
- **会议通知**: 请[订阅](https://lists.openatom.io/postorius/lists/dev.openharmony.io)邮件列表 dev@openharmony.io 获取会议链接
- **会议纪要**：[查看历史会议纪要](https://gitcode.com/openharmony/community/tree/master/sig/sig_architecture/meetings)

### 联系方式

- **邮件列表**：[dev@openharmony.io](https://www.google.com/url?sa=E&q=mailto%3Adev@openharmony.io)
- **微信群**：NA