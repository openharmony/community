# sig_compliance
English | [简体中文](./sig_compliance_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](/zh/pmc.md).
## Overview
With the rapid development of the OpenHarmony community, more and more patches are submitted by developers, more and more third-party open source software is introduced into the community, Meanwhile, OpenHarmony Compliance risks are increasing. As we all know, The community has introduced and developed [Open Source Compliance Audit Tool OAT](https://gitee.com/openharmony-sig/tools_oat), sensitive word scanning tools, open source code fragment scanning, and 7-cai tools to solve the basic compliance problems. However, there is still a lot of work to be confirmed by the team. As the size of the community increases, this will pose a huge challenge to the compliance of the community. Therefore, we hope to setup the sig_Compliance . With the SIG, we will strengthen multi-party connectionst, embrace the best practices in open source, and establish a mechanism and engineering system for open source compliance governance, including standards/norms, processes , tools, organization. The SIG will provide open source compliance governance solutions or services to organizations and individuals participating in the community.
## SIG group work objectives and scope
### work goals
- Establish OpenHarmony's open source compliance engineering system
- Formulate the rules, norms and processes of OpenHarmony's open source compliance governance
- Develop OpenHarmony's open source compliance Audit tools
- Provide OpenHarmony's open source compliance services
### work scope
The first phase of the core work of the SIG focuses on the construction of community ** open source compliance governance engineering systems and capabilities**. According to the life cycle of open source software and community development, we divide open source compliance into four categories:
- **Reliable source** (third-party open source software, community self-developed code)
- **License compliance** (open source software license compatibility, open source software license obligation fulfillment, The License Compliance of Project)
- **Intellectual Property Compliance** (Copyrights, Patents, Trademarks, Terminology)
- **Release Compliance** (Trade Compliance, The License Compliance of Release)

The work of this group **includes** 
- **Planning and developing of engineering capabilities and tools**
- **Drafting and formulation of compliance process rules**
- **Collaborate with community and industry organizations on engineering capabilities**
- **Introduction and external sharing of best practices in compliance governance**
- **Compliance culture and training within the community**

#### **Relationship between Open Source Audit Tool Project**:
As a umbrella project, The sig_compliance will 
integrate with [OAT](https://gitee.com/openharmony-sig/tools_oat) as one of most important tool for our project. Meanwhile, the other compliance tools also will be integrate into our project. We will leverage these tools to empower openharmony compliance engineering system

#### **Relationship with Open Source Compliance Group under the Openharmony Working Committee**:
In principle, this SIG should implement the compliance engineering capabilities under the guidance of the open source compliance group, and regularly report to the open source compliance group.

This group **does not** includes
- Official announcement for compliance event and legal issues
- Final interpretation of community open source compliance and legal issues
- Final desicion of community open source compliance governance standards and process

### The repository 
- project name:
  - OAT ：https://gitee.com/openharmony-sig/tools_oat


## SIG Members

### Leader
- @jalenchen(https://gitee.com/jalenchen)

### Committers
- @king-gao (https://gitee.com/king-gao)
- @alec-z (https://gitee.com/alec-z)
- @kubigao (https://gitee.com/kubigao)
- @billwangliang (https://gitee.com/billwangliang)
- @youthdragon (https://gitee.com/youthdragon)
- @jungle8023 (https://gitee.com/jungle8023)
- @yishuangli（https://gitee.com/yishuangli）
- @Rahul Mohan G（rahulmohang@gmail.com）
- @Carlo Piana（ piana@array.eu ）
- @alpianon（https://gitee.com/alpianon）

### Meetings
 - Meeting time: Public meeting time: Beijing time, every Friday afternoon, 14:00~15:00
 - Meeting application: [OpenHarmony sig_compliance Meeting Proposal](https://etherpad.openharmony.cn/p/compliance)
 - Meeting link: [Meeting link](https://etherpad.openharmony.cn/p/compliance)
 - Meeting notification:  Please [Subscribe](https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the conference link
 - Meeting-Minutes: [Archive link address](https://gitee.com/openharmony-sig/sig-content)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Zulip group：https://zulip.openharmony.cn
- Wechat group：NA
- Mailing list tag:[compliance]
