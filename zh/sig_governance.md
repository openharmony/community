**SIG 管理指南**

该文档是 OpenHarmony 社区中的 SIG（Special Interest Group）管理指南初稿。为了保证 SIG 的有效管理和发展，该文档提供了申请新 SIG 的具体流程以及仓库管理和孵化准出的操作指南。
# 1.  **申请创建新SIG流程**
为了保证OpenHarmony社区中SIG的有效管理和发展，需要有规范的流程和评审机制进行支撑，以下是申请新SIG的具体流程：
## 1.1  梳理SIG组工作目标和范围
在申请新的SIG之前，需要先梳理好该SIG组的工作目标和范围。这个步骤是为了确保SIG组的工作方向和范围能够清晰地呈现，同时也为后续的申请做好准备。
参考SIG申请[模板](../meeting-notes/docs/openharmony_sig_template.pptx)，该模板中包含了申请时需要填写的相关信息和要求。
## 1.2  提交SIG申请议题
在完成SIG申请模板的填写后，需要将[申请议题](https://docs.qingque.cn/s/home/eZQB8yRFQfEFeAxk\_6JKZEE0q?identityId=1tbICPd8j3s)提交给OpenHarmony社区的PMC。该步骤的主要作用是让OpenHarmony社区的PMC能够对该申请进行初步审核。

## 1.3  PMC会议评审
当PMC会议通过SIG申请议题时，即可进行如下步骤操作。
### 1.3.1  创建自己的新申请SIG：
首先需要将OpenHarmony社区的代码库Fork到自己的Gitee下，并在sig目录下创建自己的SIG文件夹，再将SIG申请模板（sig_template）拷贝到该文件夹下。使用SIG模板创建自己的新SIG，并根据需要进行信息填写。

```
git clone https://gitee.com/YOURGITEE/community

cd ./community/sig

cp -r sig_template sig_YOURSIGNAME

cd sig_YOURSIGNAME
```

### 1.3.2  新申请SIG组信息填写
在创建好自己的新SIG之后，需要根据需要完成新SIG组的信息填写。为便于更好的理解和填写SIG申请模板里的内容，建议先参考已有SIG的描述和说明。

```
mv sig_template_cn.md sig_YOURSIGNAME_cn.md
mv sig_template.md sig_YOURSIGNAME.md
vim sig_YOURSIGNAME_cn.md
vim sig_YOURSIGNAME.md
```

 ###  1.3.3 新SIG组织信息配置
在完成新SIG组的信息填写后，还需要完成新SIG组织信息的配置。这个配置文件将会被用于后续SIG组仓库的创建，因此需要准确填写。

```
vim sig/sigs\_list.toml
```

### 1.3.4 SIG组运作规范：
SIG组需要定期召开例会，讨论和总结SIG组领域工作，并向OpenHarmony PMC组织进行定期汇报。如果SIG组中的Leader角色有变动，需要及时知会OpenHarmony社区PMC成员，并对组织信息和仓库权限进行相应的调整。

# 2.  **仓库管理**
## 2.1  SIG组仓库新增、退休、更名申请：
### 2.1.1  申请架构SIG评审
参考[模板1--新增、退休、更名](../sig/sig_architecture/meetings/repository_review_template.pptx)准备对应的申请材料，申请架构SIG议题评审。

参考[模板2--开源软件引入](../sig/sig_architecture/meetings/OpenHarmony_thirdparty_opensource_software_selection_analysis_templateV1.0.pptx)准备对应的申请材料，申请架构SIG议题评审。

###  2.1.2 新增仓电子流申请：
[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” --> "SIG管理" --> “SIG仓申请”。
###  2.1.3 仓库退休、更名电子流申请：
[操作指导](http://ci.openharmony.cn/workbench/ciCommunity)：“操作指南” --> "SIG管理" --> “仓管理”。

##  2.2 SIG孵化准出：
###  2.2.1 申请架构SIG孵化预审：
[申请议题](https://shimo.im/sheets/StzhuFkEk38enrnl/MODOC)进行孵化准出架构预审，参考[模板](../sig/sig_architecture/meetings/repository_review_template.pptx) 准备对应的申请材料。

### 2.2.2 申请质量SIG孵化准出评审：
[申请议题](https://shimo.im/sheets/6QqqWJX99xrWWqJg/MODOC)：进行孵化准出评审，参考[准出标准](../sig/sig_qa/guidance_for_incubation_project_graduation_cn.md)准出孵化准出材料。
###  2.2.3. 提交仓库孵化准出电子流：
质量SIG准出评审通过后，提交[孵化准出电子流](http://ci.openharmony.cn/workbench/ciCommunity)： “操作指南” --> "SIG管理" --> “孵化报告”。