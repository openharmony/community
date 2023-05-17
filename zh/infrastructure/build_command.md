# OpenHarmony社区Pull Request&Issue评论支持命令清单

[Pull Request评论支持命令清单](#pull-request评论支持命令清单)

[Issue评论支持命令清单](#issue评论支持命令清单)

[Pull Request标签说明](#pull-request标签说明)

[Issue标签说明](#issue标签说明)

## Pull Request评论支持命令清单

| 评论输入命令                            | 是否必选   | 使用场景                                                                                                                                                         | 命令触发角色                               |
| --------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------ |
| start build                       | **必选** | 触发编译构建测试<br>构建门禁通过后，CI Bot会提醒审核检视人员处理PR                                                                                                                      | PR创建人<br>Committer                   |
| stop build                        | 可选     | 停止编译构建测试                                                                                                                                                     | PR创建人                                |
| submit                            | 可选     | 自动合入异常时，手工触发合入，检查通过后自动合并PR<br>检查通过条件：openharmony_ci测试通过+PR允许合入                                                                                               | 任何人                                  |
| check dco                         | 可选     | DCO检查失败时，更新DCO信息后，人工触发检查DCO<br>检查通过条件：已签署DCO+PR所有提交均包含Signed-off-by信息。可参考[DCO FAQ](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/FAQ.md)处理 | PR创建人                                |
| static-check                      | 可选     | 静态检查失败时，手工触发静态检查，仅用于单独验证，不影响最终构建结果                                                                                                                           | PR创建人                                |
| assign [@gitee_id1 @gitee_id2...] | 可选     | Committer分配检视人员，可以通过空格分割来指定多个检视人员；如果命令中不指定gitee_id，committer安排自己为检视人员。<br>分配的检视人员需参与检视，给出检视意见，然后评论命令check comment提醒PR提交人处理；无检视意见时，评论命令lgtm，提醒committer审核处理   | Committer                            |
| unassign @gitee_id                | 可选     | 取消分配检视人员                                                                                                                                                     | Committer                            |
| lgtm                              | 可选     | 如果使用assign命令分配了检视人员，PR检视人员无检视意见时，需评论该命令提醒committer可以合入对应的PR。分配多个检视人员时，需要每个检视人员都评论命令lgtm，才会提醒committer可以合入对应的PR                                               | 通过assign命令分配的检视人员PR检视人员<br>Committer |
| check comment                     | 可选     | 如果检视人员提交了检视意见，需评论该命令来提醒PR创建人修改检视意见                                                                                                                           | PR检视人员<br>Committer                  |
| code review                       | 可选     | 如果代码仓没有配置测试门禁，需评论该命令来提醒代码仓committer进行代码检视                                                                                                                    | PR创建人                                |

## Issue评论支持命令清单

| 评论输入命令        | 是否必选 | 使用场景                                                                                                             | 命令触发角色                 |
| ------------- | ---- | ---------------------------------------------------------------------------------------------------------------- | ---------------------- |
| close         | 可选   | Committer审核issue，认定为非问题、重复问题、评审不解决时，通过该命令告知issue提交人要关闭对应的issue。CI Bot会把issue标签设置为waiting_on_author               | Committer<br>仓库成员等审核人员 |
| check comment | 可选   | 审核人员认定issue缺少信息，评论需要补充哪些信息后，再评论该命令，issue会打回给issue提交人补充信息。CI Bot会把issue标签设置为waiting_on_author                     | Committer<br>仓库成员等审核人员 |
| check update  | 可选   | 标签为waiting_on_author时，issue提交人补充信息后，通过评论该命令，CI Bot会把issue标签设置为waiting_for_assign（未分配责任人）或waiting_for_fix（已分配责任人） | Issue提交人               |

## Pull Request标签说明

在PR检视审核过程中，CI Bot会为PR设置处理状态标签，用于标识处理阶段。处理阶段包含：PR提交人处理阶段，检视人员分配阶段，检视人员检视阶段，等待审核合入阶段和已合入阶段。

| 标签                 | 标签说明                     | 触发命令、条件                                     |
| ------------------ | ------------------------ | ------------------------------------------- |
| waiting_on_author  | 需要贡献者修改检视意见或门禁未通过等。      | start build门禁失败<br>check comment            |
| waiting_for_review | 等待Committer指定检视人员检视提交的PR | start build门禁成功<br>代码仓没有配置门禁时，评论code review |
| reviewing          | 已分配检视人员，处于代码检视阶段         | assign [@gitee_id]分配检视人员                    |
| waiting_for_merge  | 检视人员无检视意见，已同意合入。         | 检视人员评论lgtm                                  |
| merged             | PR已经合并                   | 审核者合入                                       |

除了上述处理状态标签，PR还支持其他标签，下表是部分支持的标签：

| 标签              | 标签说明               | 触发命令、条件          |
| --------------- | ------------------ | ---------------- |
| dco检查成功/dco检查失败 | DCO签署状态标签。         | 提交PR或check dco命令 |
| XX成功/失败         | 静态、门禁、格式化检查的成功失败状态 | start build门禁    |

## Issue标签说明

在issue检视审核过程中，CI Bot会为issue设置处理状态标签，用于标识处理阶段。处理阶段包含：issue提交人处理阶段，issue责任人分配阶段，Issue责任人修复阶段和已闭环阶段。

| 标签                 | 标签说明                                         | 触发命令、条件                     |
| ------------------ | -------------------------------------------- | --------------------------- |
| waiting_on_author  | 需要issue 提交人修改Issue，补充信息等；<br>需要issue 提交人确认验收 | 审核者通过close命令返回issue提交人修改    |
| waiting_for_assign | 需要issue审核者分配责任人处理issue                       | Issue提交人创建issue后，且创建时未指定责任人 |
| waiting_for_fix    | issue在修复中                                    | Committer分配了责任人或关联了PR       |
