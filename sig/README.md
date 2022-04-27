# SIG管理章程
简体中文 | [English](./README-EN.md)

## 背景
 1. SIG（Special Interest Group）是指特别兴趣小组，SIG在PMC项目管理委员会指导下，负责OpenHarmony社区特定子领域及创新项目的架构设计、开源开发及项目维护等工作。
 2. 为了便于OpenHarmony开源社区工作开展和交流，默认将其划分为23个初始的SIG小组：[Maps_Sigs_Subsystem](./sigs_subsystem_list.md)。
 3. 本目录用于存放OpenHarmony社区所有 “特别兴趣小组”（Special Interest Group，以下简称 SIG）的运作信息。

## SIG职责&运作方式
 1. 领域的技术演进方向由SIG组承担，负责领域技术竞争力分析和关键技术识别及决策。
 2. 负责领域内功能分解分配，模块间接口定义与维护管理。
 3. 社区的工作实体是SIG组，从基础设施到OS部件，从测试系统到版本发布都是由不同SIG的来承担。
 4. 一个良好的社区组织形式是持续运作的关键，仪式感很重要，SIG组需要通过周期例会来保持其有效的运作，并定期向PMC委员会汇报进展。

## 申请新建SIG
 1. 开发者在社区中寻找2-3个以上有共同兴趣及目标的人，确定SIG Leader。参考[新建SIG Charter](sig-template/sig_template_cn.md)模板，创建SIG Charter提案，提案包括如下要素：
     - 创建SIG的背景信息
     - 创建SIG的业务范围
     - 创建SIG的业务目标
 2. **那些情形适合申请创建SIG**:
     - 发起的申请属于OpenHarmony社区中的已有的技术方向, 建议直接参与到已创建的SIG组中进行共建；
     - 发起孵化的技术项目, 能代表某一个领域的技术方向, 并最终能转化为OpenHarmony的新增部件；
 3. SIG Leader以[SIG-Charter-Proposal-XXX]为邮件标题，需先订阅[dev@openharmony.io](https://lists.openatom.io/postorius/lists/dev.openharmony.io/)，将申请材料以附件方式向dev@openharmony.io发送邮件，提交新建SIG申请。
 4. PMC或对应领域SIG、Committer邮件回复同意后，然后向[PMC](https://etherpad.openharmony.cn/p/pmc)申报议题，PMC会根据收到的议题统一安排SIG申请评审，PMC根据评审通过后，申请者按照评审意见完善后，向[Community](https://gitee.com/openharmony/community)仓创建新的SIG的Pull Request申请新建SIG。
     - **重要**：SIG中如需新建仓申请的，请向[架构SIG](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC)中申报新增部件的议题。

## 加入已有SIG
1. 开发者可通过SIG列表查看感兴趣的SIG，通过订阅邮件列表、参与SIG会议等形式，参与对应SIG项目的技术讨论、社区维护及开源开发。

## 运营维护SIG
1. SIG Leader Fork OpenHarmony/community分支，在SIG文件夹下，以新SIG名称新建文件夹，并参考[SIG模板](sig-template/)，创建对应的SIG配置文件，提交PR合入申请。
2. SIG孵化子项目，统一存放在[OpenHarmony SIG组织](https://gitee.com/openharmony-sig)，待孵化成熟后，可合入OpenHarmony组织代码主库。
3. SIG Leader及Committer负责对应SIG的运营及维护，会议纪要和资料统一参考sig-template目录下的[meetings](https://gitee.com/openharmony-sig/sig-content)和[docs](https://gitee.com/openharmony-sig/sig-content)模版进行归档。
4. SIG Leader定期在PMC项目管理委员会汇报SIG孵化项目及SIG运营进展，PMC基于SIG运作情况给出指导建议。

## SIG孵化项目毕业
 1. SIG孵化项目成熟并满足项目毕业要求后，可申请合入OpenHarmony组织代码主库。
 2. SIG Leader通过向dev@openharmony.io发送邮件，提交孵化项目毕业申请。
 3. PMC项目管理委员会通过项目毕业申请后，社区接纳孵化项目合入OpenHarmony主干。
 4. 孵化项目毕业评审请按照[要求自检](./sig-QA/guidance_for_incubation_project_graduation_cn.md)。

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
