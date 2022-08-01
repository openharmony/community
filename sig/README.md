# SIG管理章程
简体中文 | [English](./README-EN.md)

# OpenHarmony社区SIG管理制度
本文档主要介绍OpenHarmony社区SIG（Special Interest Group）的管理制度，包括申请新SIG和SIG的运营、变更及终止。

## 一、申请新SIG

### 1.申请准备

- 开发者需仔细阅读[SIG管理制度]，了解OpenHarmony社区SIG的运作规则，提前准备好下文所述的SIG章程、SIG制度等文档；
- 开发者可通过[OpenHarmony zulip相关频道](https://zulip.openharmony.cn/join/u7vafdcbyia32bsssygwbbee/)提前告知社区新建SIG的意向，寻找兴趣相投的开发者共同参与；
- 申请新SIG需确认其技术方向的唯一性与可行性：
- OpenHarmony社区每个SIG孵化的技术方向都不同，发起的申请如果属于OpenHarmony社区已有的技术方向，则会被建议直接参与相关SIG共建；
- 开发者可查看OpenHarmony社区[已有SIG列表](https://gitee.com/openharmony-sig)，同时查看[历史DEV邮件列表](https://lists.openatom.io/hyperkitty/list/dev@openharmony.io//)，以确认没有相同技术方向的SIG存在或处于申请中；
- 申请成立SIG的技术项目应能够最终转化为OpenHarmony的新增部件；
- 如查阅相关信息后仍对技术方向问题存有疑虑，开发者可通过邮件列表dev@openharmony.io咨询PMC。

### 2.提交申请
SIG发起人参照[SIG章程模板]创建SIG提案初稿，以附件形式发送给dev@openharmony.io，邮件标题为：
- **SIG-Charter-Proposal-SIG XXX+简要介绍**，如`SIG-Charter-Proposal-SIG Test+OpenHarmony开发自测试能力构建`。

### 3.PMC评审提案
- SIG发起人接受PMC问询，对SIG提案进行必要的说明，并根据PMC的指导意见修改提案，通过原申请邮件与PMC进行沟通，直至PMC无疑问；
- 初审过程中，SIG提案可能会因为不符合OpenHarmony社区整体技术规划或已有相关技术方向的SIG存在而被拒绝；
- 收到PMC邮件回复同意后代表初审通过，SIG可发起人[申报PMC例行会议新建SIG议题](https://etherpad.openharmony.cn/p/pmc)，按时接入PMC会议，介绍待新建的SIG，并请PMC批准SIG成立以及相关SIG仓库和沟通渠道的建立；
- 评审会议形成会议纪要并附PMC评审意见。

### 4.提交PR 
SIG发起人收到PMC评审反馈、确认SIG提案通过后，执行以下操作：
- fork OpenHarmony社区仓库到本地，在`OpenHarmony/community/sig`仓库内新建SIG文件夹，文件夹名称为“sig-XXX”；
- 创建该SIG的`README.md`、`OWNERS.md`文档，文档格式请参考[其他SIG](https://gitee.com/openharmony/community/tree/master/sig)，如sig-driver的[README.md](https://gitee.com/openharmony/community/blob/master/sig/sig-driver/sig_driver_cn.md)及[OWNERS.md](https://gitee.com/openharmony/community/blob/master/sig/sig-driver/OWNERS)。
- 更新`sigs.json`文档，参考以下样例： 

**sigs.json 文件格式**
| 字段 | 说明 |
|:---|:---|
| sig-name | SIG名称 |
| projects| gitee仓名 |
| project-path | OpenHarmony下的归档路径，若不涉及回合OpenHarmony填写NONE |

**sigs.json 样例**
```
"sigs-List":[
{
"sig-name":"sig-python",
"projects":"https://gitee.com/openharmony-sig/python",
"project-path":"python/"
},
{
"sig-name ":"sig-updates",
"projects":["https://gitee.com/openharmony/startup_appspawn_lite", "https://gitee.com/openharmony/startup_bootstrap_lite"]
"project-path":["base/startup/appspawn_lite", "base/startup/bootstrap_lite"]
},
]
}
```
完成上述文档创建、更新后，SIG发起人提交一个Pull Request（PR），请求将以上更新合入主干，PR中附PMC评审意见等相关资料。 

该PR由Community仓的Committer审核通过后，相关更改被合并至Community仓，新SIG成立。

## 二、SIG运营

### （一）SIG仓库及沟通渠道
1. SIG使用社区统一基础设施开展工作和交流，包括Gitee仓库和邮件列表。 
2. 新SIG负责人在[OpenHarmony/community仓库](https://gitee.com/openharmony/community)提交Issue，申请为该SIG新建仓库及邮件列表。 
3. Issue中应注明仓库路径、邮件列表名称以及新SIG的Leader和Committer，并附[前述PMC评审意见](#3.PMC评审提案)，通过在Issue中[@wanchengzhen](https://gitee.com/wanchengzhen)或[@im-off-this-week](https://gitee.com/im-off-this-week)通知Sig Architecture评审。
4. Sig Architecture评审通过后：
- SIG负责人联系[社区代码仓管理员](https://gitee.com/landwind)执行建仓操作；
- SIG负责人联系[邮件列表负责人](likang@openatom.org)创建邮件列表：
- 需详细说明邮件列表名称和管理员邮箱（一般为SIG负责人），
- 邮件列表创建成功后，SIG负责人进入[OpenHarmony项目群邮件列表登陆页面](https://lists.openatom.io)，通过管理员邮箱登录后可管理邮件列表（批准成员加入或审核邮件等），其他人可订阅查看。
5. SIG可根据需要自行组建微信群等其他社交群组。 

### （二）完善SIG制度文档
1. SIG章程与制度文档需遵循OpenHarmony社区章程与相关制度。
2. 每个SIG至少要有`README.md`、`OWNERS.md`二个文档，详细说明SIG的工作范围、工作目标、成员、沟通方式、决策机制、例行会议时间、如何参与贡献等，且需要PMC批准。 
3. SIG如有特殊贡献文档，需遵循[OpenHarmony社区贡献原则](https://gitee.com/openharmony/docs/blob/master/zh-cn/contribute/Readme-CN.md)。

### （三）SIG成员及职责 

SIG的主要成员是Leader和Committer，每个SIG初始成员不少于3人。 

`README.md`、`OWNERS.md`文档中需详细列出SIG Leader和Committer。SIG Leader和Committer的更换及任命需PMC批准。SIG可根据需要增加其他岗位角色，但需PMC批准。 

#### **1.Leader**
每个SIG至少有1名Leader。 
作为SIG组的管理者，Leader负责SIG的运营及维护，同时直接参与上游或周边组织的协调。 
初始Leader由SIG创建时指定，后继人选从Committer中选出。 
如SIG组内暂无Committer或人数较少，Committer的职责由Leader兼任。SIG Leader拥有SIG子领域的代码仓管理员权限。

**主要职责：**
- 定义SIG的工作范围及业务目标。
- 确定SIG的技术路线：包括规划和决策SIG技术方向、路标规划、架构演进。
- 吸纳并发展Committer参与SIG的项目孵化、文档完善及社区推广。
- 定期在PMC会议中汇报SIG孵化项目及SIG运营进展，并基于PMC的指导建议完成相关改进。
- 召集SIG组会议：定期召集SIG组会议，决策SIG组内上升的争议。
- 参与社区协调活动：作为SIG的代表参与社区活动和特定会议。

#### **2.Committer**
每个SIG至少有2名Committer。 
初始Committer由SIG创建时指定，后继人选从社区Contributor中选出，由Leader和Committer提名、SIG当前贡献者全体投票表决产生。 
Committer负责代码审核、主干代码合入及特性设计方案审核和批准，拥有SIG子领域的代码仓写入权限。 

**主要职责：**
- 处理SIG内及社区与本SIG相关的Issue、PR、邮件列表问题等。
- 辅导Contributor快速理解SIG领域架构设计并提升代码开发技能。
- 跟踪依赖性问题：修复因代码更新导致的本SIG内被破坏的依赖关系。
- 对本SIG内的安全问题进行分类和处理，参与安全团队的安全问题，维护SIG组内的安全规范和要求。 

### （四）SIG治理

#### 1.会议组织
- SIG需定期召开例行会议，每双周至少半小时，由SIG Leader主持；
- 会议议程提前在邮件列表及官网进行公布；
- 会议纪要及时发布并保存在`OpenHarmony/community/sig/sig-XXX/meeting-minutes`内。

#### 2.社区共建
- SIG Leader至少两个月一次，在PMC例会汇报SIG工作进展，并基于PMC指导意见改进工作；
- SIG每年至少一次，由SIG Leader向社区报告SIG年度工作进展；
- 协助存在关联关系的周边SIG，联合完成临时性工作；
- 基于社区定期的SIG成果评估，表现优秀的SIG将被邀请参加社区版本发布会议。

#### 3.技术决策
- SIG内的决策遵循OpenHarmony社区的治理模式。
- SIG内采用“懒惰共识”（沉默即同意）的方式进行决策：
- 如存在争议时，由包括Leader在内的全体Committer进行投票表决，以多数票通过的形式达成共识；
- 无法在SIG内达成共识时，可上升至PMC决策。

## 三、SIG变更

### （一）增删项目或仓库
1. SIG负责人在PMC例行会议中申报议题，接受PMC问询。 
2. PMC批准增删项目或仓库后，SIG负责人：
- 在`OpenHarmony/community`创建Issue请求SIG Architecture支持，完成新项目仓库的配置或删除仓库，Issue中附PMC评审意见；
- 相关操作完成、Issue关闭后，更新`sigs.json`文档（参考[上文](#4.提交PR)），刷新`README.md`；
- 提交PR请求合并以上修改，PR中附PMC评审意见。 
3. Community仓的Committer合并PR，完成项目或仓库更新。 

### （二）修改SIG名称、章程、成员等

#### 涉及SIG工作范围、成员变更等重大变更
1. SIG负责人在PMC例行会议中申报议题，接受PMC问询。 
2. PMC批准变更后，SIG负责人：
- fork的`OpenHarmony/community/sig`的相关SIG文件夹内刷新`README.md`、`OWNERS.md`、等文档；
- 提交PR，请求合并以上修改，PR中附PMC评审意见。 
3. Community仓的Committer审核并合并PR，确认变更。

#### SIG内的非重大变更
1. SIG负责人：
- fork的`OpenHarmony/community/sig`文件夹下找到相关SIG文件夹，完成修改；
- 刷新README.md等文档；
- 提交PR，请求合入以上修改。 
2. Community仓的Committer审核并合并PR，确认修改。 

区分变更重大与否的标准可参考上文[SIG的运营部分](#二、SIG运营)。

## 四、SIG终止

### （一）以下情况将触发SIG终止申请： 
1. SIG已达到预期目标，无需再投入； 
2. SIG未达成预期目标，超过2个月不活跃； 
3. SIG违反OpenHarmony社区PMC或SIG制度； 
4. SIG Leader、Committer等成员流失，无法支撑SIG正常工作。 

### （二）SIG QA定期检查各SIG状态，并定期在PMC会议中汇报各SIG活跃度：
1. 对于已达到预期目标的SIG，由SIG Leader通过邮件列表dev@openharmony.io提交SIG终止申请，PMC评估后进行终止操作。 
2. 对于未达到预期目标但不活跃的SIG，PMC委派PMC成员进入该SIG进行尽职调查，并组织SIG整改，整改时间2个月。SIG超过2个月依然不活跃时，由SIG Leader或QA-SIG Leader提交SIG终止申请，PMC评估后进行终止或合并操作。

### （三）终止流程：
1. 向dev@openharmony.io发送电子邮件，通知社区解散或合并SIG。 
2. SIG负责人在`OpenHarmony/Community`下创建一个PR，请求合并以下更改： 
- 归档代码仓（[归档地址](https://gitee.com/openharmony-retired)）
- 删除SIG共享日历，确保已上传所有SIG会议回放及会议纪要（`OpenHarmony/Community/archive/sig-XXX/meeting-minutes`）。 
- 将现有Community仓的SIG目录移至`OpenHarmony/Community/archive`文件夹内。 
- 将SIG内每个子项目的所有权转让给项目外部的新SIG，或者直接废弃子项目； 
- PMC决策合并SIG后，原SIG相关交付件由原SIG Leader按时按质交接给新SIG Leader，交接期为一个月。 
- 停用或转移主仓库下的SIG仓。 
- 停用或通过SIG-Testing转让SIG内所有测试基础设施作业。
- 删除或弃用SIG的所有标签。
- 删除或重命名任何引用该SIG的社区组织。
- 更新`sigs.json`文档。

## SIG数据存放和管理方式
SIG信息记录统一归档在OpenHarmony/community仓库的sig目录内：
1. sig_xxx.md/sig_xxx_cn.md：包括SIG组工作目标和范围、SIG管理的repository及描述、SIG组织会议、SIG成员。

2. sigs.json：为了便于工具自动提取，其中SIG的maintainer/committer信息单独备份一份至OWNER文件内，每个SIG所维护的仓库名称列表/目录结构位于sigs.json文件中。
    - OpenHarmony/community仓的sig目录下存在一个sigs.json文件，这个文件中管理从PMC看到的所有SIG的信息。
    - sigs 由 PMC 修改和维护，新sig申请由对应的 maintainer 提交PR，经过PMC审视后合入。
    - sig 独立目录下的sig_xxx_cn.md/sig_xxx.md 为 sig 的信息展示区。其中SIG基本信息需按模板留空，新建SIG时填写完整。
    - sig 独立目录下的OWNER存放相应sig的maintainer。
  
3. 代码的管理
    - 代码在[sig-manifest仓](https://gitee.com/openharmony-sig/manifest)下统一管理。
    
    - 需要各leader维护本组内对应仓的 .xml 文件。
    
    - 多个单位参与，可向leader提出建仓需求，由leader向社区提建仓pr。
  
4. 文档的管理
    - 各sig组的公共文档（包括会议纪要、会议材料等）需放入[sig-content](https://gitee.com/openharmony-sig/sig-content) 仓对应组的文件夹内。
    - 与各sig组子任务密切相关的技术文档可放到任务对应的代码仓内。
  
5. 任务进度

    - 任务进度以在对应任务仓下提issue形式更新。
    - 作为跟踪进度的issue需要打上特定的标签，标签暂定为 **sig_taskprogress**。

6. 开源协议的选择
   - 建议开发者使用Apache 2.0 开源协议。  


###  sigs.json 文件格式
| 字段 | 说明 |
|:---|:---|
|  sig-name | SIG名称 |
|  projects| gitee仓名 |
|  project-path | OpenHarmony下的归档路径，若不涉及回合OpenHarmony填写NONE |

### sigs.json 样例
```
"sigs-List":[
      {
         "sig-name":"sig-python",
         "projects":"https://gitee.com/openharmony-sig/python",
         "project-path":"python/"
      },
      {
         "sig-name":"sig-updates",
         "projects":["https://gitee.com/openharmony/startup_appspawn_lite", "https://gitee.com/openharmony/startup_bootstrap_lite"],
         "project-path":["base/startup/appspawn_lite", "base/startup/bootstrap_lite"]
      },
   ]
}
```
