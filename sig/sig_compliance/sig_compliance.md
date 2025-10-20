# sig_compliance
English | [简体中文](./sig_compliance_cn.md)

Note: The content of this SIG follows the convention described in OpenHarmony's PMC Management Charter [README](../../zh/pmc.md).
## Overview
With the rapid development of the OpenHarmony community, more and more patches are submitted by developers, more and more third-party open source software is introduced into the community, Meanwhile, OpenHarmony Compliance risks are increasing. As we all know, The community has introduced and developed [Open Source Compliance Audit Tool OAT](https://gitcode.com/openharmony-sig/tools_oat), sensitive word scanning tools, open source code fragment scanning, and 7-cai tools to solve the basic compliance problems. However, there is still a lot of work to be confirmed by the team. As the size of the community increases, this will pose a huge challenge to the compliance of the community. Therefore, we hope to setup the sig_Compliance . With the SIG, we will strengthen multi-party connectionst, embrace the best practices in open source, and establish a mechanism and engineering system for open source compliance governance, including standards/norms, processes , tools, organization. The SIG will provide open source compliance governance solutions or services to organizations and individuals participating in the community.
## SIG group work objectives and scope
### work goals
- Establish OpenHarmony's open source compliance engineering system
- Formulate the rules, norms and processes of OpenHarmony's open source compliance governance
- Develop OpenHarmony's open source compliance Audit tools
- Provide OpenHarmony's open source compliance services
### work scope
#### Phase I (Done)
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


#### Phase II (Current)
The core focus of **Phase II** of this working group is to **expand** upon the established community open source compliance governance engineering system and capabilities, with new emphasis on OpenHarmony SBOM (Software Bill of Materials) management and governance of third-party open source software introductions.

- **(Existing) Open Source Compliance** 
  (Copyright/license compliance, fulfillment of open source obligations)
- **(Newly Added) SBOM Management** 
  (SBOM generation, data governance, format standardization, lifecycle management, access control)
- **(Newly Added) Third-party Open Source Software Introduction Governance** 
  (Introduction review: legal compliance, lifecycle assessment, technical ecosystem alignment, source credibility; metadata governance, lifecycle management)

The working group's responsibilities encompass the following areas under the above categories:
- **Planning and development of engineering capabilities and tooling** 
- **Drafting process guidelines and regulations** 
- **Collaboration with internal community and industry organizations on engineering capabilities** 
- **Adoption and external sharing of compliance governance best practices** 
- **Fostering compliance culture and training within the community** 
- **Compliance review for third-party open source software introductions** 
- **SBOM engineering capabilities, process standards, and data governance**

#### **Relationship between Open Source Audit Tool Project**:
As a umbrella project, The sig_compliance will 
integrate with [OAT](https://gitcode.com/openharmony-sig/tools_oat) as one of most important tool for our project. Meanwhile, the other compliance tools also will be integrate into our project. We will leverage these tools to empower openharmony compliance engineering system

## Code Repository
- Repository Address:：
  - SIG-Compliance ：https://gitcode.com/openharmony/community/tree/master/sig/sig_compliance
  - OAT ：https://gitcode.com/openharmony-sig/tools_oat
  - OAT IDE pulgin：https://gitcode.com/openharmony-sig/oat_deveco_plugin
  - license compatibility：https://gitcode.com/openharmony-sig/compliance_license_compatibility
  - composition analysis： https://gitcode.com/openharmony-sig/compliance_composition_analysis
  - open source policy： https://gitcode.com/openharmony/docs/blob/master/zh-cn/contribute/OpenHarmony%E7%A4%BE%E5%8C%BA%E5%BC%80%E6%BA%90%E5%90%88%E8%A7%84%E8%A7%84%E8%8C%83%E5%8F%8A%E6%8C%87%E5%AF%BC.md


#### **Relationship with Open Source Compliance Group under the Openharmony Working Committee**:
In principle, this SIG should implement the compliance engineering capabilities under the guidance of the open source compliance group, and regularly report to the open source compliance group.

This group **does not** includes
- Official announcement for compliance event and legal issues
- Final interpretation of community open source compliance and legal issues
- Final desicion of community open source compliance governance standards and process

## SIG Members

### Leader
- @kubigao (https://gitee.com/kubigao)

### Committers
- @king-gao (https://gitee.com/king-gao)
- @kubigao (https://gitee.com/kubigao)
- @youthdragon (https://gitee.com/youthdragon)
- @Rahul Mohan G（rahulmohang@gmail.com）
- @Carlo Piana（ piana@array.eu ）
- @alpianon（https://gitee.com/alpianon） 
- 欢迎加入

### History Leader及 Committers
- @jalenchen(https://gitee.com/jalenchen) 2022-2023 SIG Leader
- @jungle8023 (https://gitee.com/jungle8023)  2023  committer
- @yishuangli（https://gitee.com/yishuangli）  2022  committer
- @billwangliang (https://gitee.com/billwangliang) 2022  committer
- @alec-z (https://gitee.com/alec-z) 2022  committer

### Meetings
 - Meeting time: Public meeting time: Beijing time, every Friday afternoon, 14:00~15:00
 - Meeting application: [OpenHarmony sig_compliance Meeting Proposal](https://shimo.im/sheets/B1Aw1d18GeFygLqm/MODOC)
 - Meeting link: [Meeting link](https://shimo.im/sheets/B1Aw1d18GeFygLqm/MODOC)
 - Meeting notification:  Please [Subscribe](https://lists.openatom.io/postorius/lists/dev.openharmony.io) mailing list dev@openharmony.io for the conference link
 - Meeting-Minutes: [Archive link address](https://gitcode.com/openharmony-sig/sig-content)

### Contact (optional)

- Mailing list：dev@openharmony.io
- Wechat group：NA- Mailing list tag:[compliance]
