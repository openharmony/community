# OpenHarmony RFC(Request for comments)流程
该目录用于存放评审通过了的RFCs，这个流程参考了[Rust的RFCs](https://github.com/rust-lang/rfcs)治理流程的成功经验。

##  RFC简介
1. 大多数变更，比如 bugfix 、文档，通过 Pull Request 完成，但是某些 “重大的” 的变更，需要通过一些设计过程，让社区达成共识。
2. RFC旨在为OpenHarmony已有的重大特性变更或新增提供开放透明和规范化的流程。通过从利益相关者和专家那里获得反馈，并广泛地交流设计变更，从而促进OpenHarmony社区成员积极地参与OpenHarmony开发工作和生态繁荣建设。

3. RFC 是描述需求与解决需求的建议更改的文档。具体来说，RFC 将：

- 根据  [RFC 模板](./yyyymmdd-rfc-template_cn.md)进行撰写。
- 作为PR请求提交到  [community/rfcs](https://gitee.com/openharmony/community/tree/master/rfcs)  目录。
- 在接受之前要经过项目仓Committer或领域SIG Leader充分讨论和会议评审，无对应SIG领域归属的，与架构SIG讨论和会议评审或转[SIG项目孵化](https://gitee.com/openharmony/community/blob/master/sig/README.md)。


## 如何提交 RFC

1. 在提交 RFC 之前，请与OpenHarmony部件维护者和贡献者充分讨论您的目标，并获得反馈。请使用OpenHarmony的开发者邮件列表或对应领域SIG邮件列表（[dev@openharmony.io 或 sig_signame@openharmony.io](https://lists.openatom.io/postorius/lists/)）。

2. 起草您的 RFC。

- 参考  [RFC 模板](./yyyymmdd-rfc-template_cn.md)。
- 将您的 RFC 文件命名为  `YYYYMMDD-description-name.md`，其中  `YYYYMMDD`  是提交日期，而  `descriptive-name`  与您的 RFC 标题相关。（例如如果 RFC 标题名称为  _Micro Python Framework_，则可以使用文件名  `20210720-micro-python-framework.md`）。
- 如果要提交图片或其他有助于理解设计的附属文档，请创建格式为  `YYYYMMDD-descriptive-name`  的目录来存储这些文件。

3. 编写 RFC 草稿后，请先征求项目仓Committer和贡献者的反馈，然后再提交。 不要求编写并实现代码，如果有代码实现将有利于研讨。

4.  招募发起人。
- 发起人必须是项目仓库的Committer或对应领域的SIG Leader，[沟通地图信息](../sig/sigs_list.toml)。
- 请先在 RFC 中注明发起人，然后再发布 PR。
-  您 _可以_ 在没有发起人的情况下发布 RFC请求，但是如果在发布 PR 请求的一个月内仍然没有发起人，则该 PR 将被关闭。

1. 将您的 RFC 作为 PR 提交到  [openharmony/community/rfcs](https://gitee.com/openharmony/community/tree/master/rfcs)。

2. 通过开发者邮件列表向开发者发送简要说明、PR 链接和审查请求，邮件标题加前缀[RFC]。

3. 发起人将在 RFC PR 发布后的两周内请求召开SIG技术评审会议。评审会议的目的是解决小的争议，大争议应提前达成共识。如果评审过程中提出了问题，请等到问题解决后再重新发起进行评审。

4. 会议可以接受或拒绝 RFC，也可以待更改后重新评审。评审通过的 RFC 将合并到  [community/rfcs](https://gitee.com/openharmony/community/tree/master/rfcs  中， 而 被拒绝的RFC 的 PR 则会被关闭。


## RFC 参与者

1. RFC 流程涉及到许多人员：

- **RFC 作者**  - 编写 RFC 并致力于在整个流程中倡导 RFC 的一名或多名社区成员

- **RFC 发起人**  - 发起 RFC 并在 RFC 评审过程中提供支持的项目仓Committer或SIG Leader

- **评审委员会**  - 负责建议是否被采纳 RFC 的SIG组或PMC委员会

- 任何**社区开发者**都可以通过提供有关 RFC 是否满足其需求的反馈来参与该流程。

2. ### RFC 发起人

- 发起人是负责确保 RFC 流程获得最终结果的项目维护者。职责包括：

    - 引导 RFC 符合现有平台的架构设计。
    - 引导评审委员会达成共识。
    - 当评审委员会请求更改时，确保更改得到妥善实施并寻求委员会成员的后续批准。
    - 当 RFC 经批准待实现时：
      - 确保建议的实现方法符合设计。
      - 与相关方进行协调以成功落实实现方案。

### RFC 评审委员会

1. RFC 评审委员会由对应的SIG和架构SIG组成，在评审协商一致的基础上决定批准、拒绝还是请求更改。责任包括：

- 确保考虑到社区反馈的真实内容。
- 添加其会议记录作为 PR 评论。
- 提供其做出决策的详细理由。

2. 评审委员会的人员构成可能会因每个项目而异。对于核心OpenHarmony部件，委员会将由在相关领域具有专业知识的SIG Leader 和Committer维护者组成。

### 社区成员和 RFC 流程

1. RFC 的目的是确保 OpenHarmony 的新变更能够很好地表示和传达社区的想法。社区成员有责任参与他们对其结果感兴趣的 RFC 的审查工作。

2. 对 RFC 感兴趣的社区成员应：

-  尽早**通读 RFC并提供反馈**，以留出足够的讨论时间。
- 以**文明且具有建设性**的方式提供反馈意见。

## 实现新功能

1. RFC 一经批准，即可开始实现 RFC。编码并实现RFC需求时应考虑：

- 请确保理解了RFC 中批准的功能需求和设计思路。在开始工作之前，尽量充分提出问题并讨论解决方法。
- 新功能必须包括新的单元测试，以验证该功能是否按预期工作。建议在编写代码之前先编写这些测试。
- 遵循  [OpenHarmony 代码样式指南](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/%E8%B4%A1%E7%8C%AE%E4%BB%A3%E7%A0%81.md)
- 添加或更新相关的 API 文档，请遵循[API治理章程](https://gitee.com/openharmony/docs/blob/master/zh-cn/design/OpenHarmony-API-governance.md)。
- 先运行单元测试，然后再提交代码。
- 与 RFC 发起人合作并实现相关代码。

## 保持高标准

1. 我们鼓励和感谢每一位贡献者的贡献，但也同时有意地保持着较高的 RFC 接受门槛。在以下任何一个阶段，新功能都可能会被拒绝或要求重大修改：

- 相关邮件列表的初始设计交流过程中。
- 未能招募到发起人。
- 沟通阶段存在重大异议。
- 在设计评审过程中未能达成共识。
- 在实现过程中出现问题（例如：无法实现向后兼容性、在维护方面存在疑虑）。

2. 如果RFC流程运行完善，那么RFC被拒绝的情况应发生在RFC的早期阶段而非后期代码实施阶段。经接纳的RFC不能作为承诺实现的保证，并且RFC实现能否最终被接纳仍然要满足代码评审阶段的要求，不满足代码评审阶段的要求i提交，项目仓的Committer可以有理由的拒绝接纳。

3. 如果您对此流程有任何疑问，请随时通过dev邮件列表提问，或在  [OpenHarmony/community](https://gitee.com/openharmony/community/issues) issue中提交问题。