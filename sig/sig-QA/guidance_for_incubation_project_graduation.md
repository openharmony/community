Graduation Review Organization for SIG Incubation Projects

English | [简体中文](./guidance_for_incubation_project_graduation_cn.md)

- After a Special Interest Group (SIG) incubation project meets the graduation requirements, the SIG leader can request a graduation review. A graduated project can be incorporated into the master code repository of the OpenHarmony community.
- To apply for a graduation review, the SIG leader shall send an email to dev@openharmony.io.
- The QA SIG shall organize the graduation review of the incubation project.

#### Graduation Review Participants

| Role|  Participant|Contact Method|
| ------------ | ------------ | ------------ |
|  Project Management Committee (PMC)|  Dong Jinguang|  [dongjinguang](https://gitee.com/dongjinguang) |
|  PMC|  Liang Kelei|  [xzmu](https://gitee.com/xzmu) |
|  PMC|  Huang Minglong|  [minglonghuang](https://gitee.com/minglonghuang) |
|  Architecture SIG| Ren Gelin| [im-off-this-week](https://gitee.com/im-off-this-week)  |
|  Security SIG|  Zhang Adong|[zhangadong](https://gitee.com/zhangadong)   |
|  Test SIG|  Nie Xin|[nie-x](https://gitee.com/nie-x)   |
|  Test SIG|  Wang Juntao| [wangjuntao](https://gitee.com/buranfanchen)  |
|  Infrastructure SIG| Wang Yiming| [youthdragon](https://gitee.com/youthdragon)  |
|  API SIG | Zhang Yongzhi| [zhangyongzhi](https://gitee.com/karl-z)|
|  CompileRuntime SIG| Wang Xing|[wangxing](https://gitee.com/wangxing-hw)   |
|  Compliance representative| Chen Yaxun| [jalenchen](https://gitee.com/jalenchen)  |
|  Operations representative| Liu Guo| [guoguoliu](https://gitee.com/guoguoliu)  |
|  QA SIG | Xing Wenhua| [xhuazi](https://gitee.com/xhuazi)  |
|  Incubation project owner|   |   |
|  Related SIGs|   |   |

#### Graduation Review Checklist

| Category| Sub-category|  Requirement| Review Mode|  Reviewer|
| ------------ | ------------ | ------------ | ------------ | ------------ |
| Basic| Documentation| The home page of the project briefly describes the functions of the project and displays the incubation status.| Tool + manual: Use the community's OSS Audit Tool (OAT) to check the README file names and their archive locations. Manually check whether these files clearly describe the functions of the project.| Docs SIG|
| Basic| Documentation|  The project provides guidance documents for building the project and archives them in an easy-to-find location.| Manual: Manually check whether the README files contain the build guide.| Docs SIG|
| Basic| Documentation| The project provides external API documents in an easy-to-find location. If the project can be directly used by end users, it also provides the corresponding user guide.|  Manual: Check whether external API documents and user guides are included.|  Docs SIG|
| Basic| Documentation| The project provides English documents, and it correctly processes issues described in English.| Manual: Check the English documents and the replies to issues in English.| Docs SIG|
| Legal affairs| Intellectual property| All source code of the project contains the license header and copyright statement.| Tool: Use OAT to check whether all project files contain correct license headers and copyright statements.| QA SIG  |
| Legal affairs| Intellectual property| The new code of the project is independently developed. If the code is committed by a third party, the commit message contains reliable code source information.|  Tool: Use the community's FOSSSCAN to scan self-developed code to ensure that no third-party code segment exists.|  QA SIG |
| Legal affairs| Intellectual property| All project committers have signed the Developer Certificate of Origin (DCO).| Tool + manual: Use a tool to check whether a code committer has signed DCO. Manually review the DCO signing request.| QA SIG  |
| Legal affairs| License| The project contains OSI licenses, and its licenses and the licenses of the software that it depends on do not add more restrictions than the licenses of the OpenHarmony project do.|   Tool + manual: Use OAT to check the compatibility of the project licenses. If there is any problem, manually confirm with the lawyer.| QA SIG  |
| Legal affairs| License|The libraries on which the project depends are open-source software and can be obtained publicly.|  Tool + manual: Use FOSSSCAN to scan the code for matching with third-party code, and manually check whether the software is open source.| QA SIG  |
| Legal affairs| License| The project's license file is in the required location in the project repository, and its name conforms to the community specification.| Tool: Use OAT to check the license file of the project.| QA SIG  |
| Project operations| Issue response|The project provides issues for tracking, and properly classifies and rates the registered issues.|  Manual: Manually review the issue list.| SIG Owner  |
| Project operations| Issue response| The project has responded to most issues (> 80%) in the past 2 to 12 months.| Tool + manual: Use the community's issue platform to collect statistics on issue closure. Manually review the statistics.| SIG Owner  |
| Project operations| Issue response| The initial response time for any vulnerability report of project-involved third-party software received by the project in the past six months is less than or equal to 14 days.| Manual: Manually review the response record of vulnerability reports.| SIG Owner  |
| Collaboration| Culture|The project maintains a public list of contributors who have the decision-making right. All important discussions of the project are recorded in written form on the formal communication channel of the project. For issues on which consensus cannot be reached through internal discussion, a community-wide open vote is organized to reach consensus.| Manual: Manually review project meeting minutes.| SIG Owner   |
| Quality| Buildability| The project supports building of a workable system from the source code by using only publicly available build tools in the industry.| Tool + manual: Check whether an automatic build can be quickly completed by referring to the build guide.|  CompileRuntime  SIG |
| Quality| Buildability|The project supports integration with the existing tool chain of the community.|  Manual: Manually review CI building results.| QA SIG  |
| Quality| Testability| The project provides complete test cases, covering most logic branches and all external interfaces. It also supports integration with the community's test suite for automated testing.| Tool: Use the automated test suite to cover over 85% of the test cases.| Test SIG  |
| Quality| Compatibility|The project clearly records any incompatible changes, and provides tools and documents to help users upgrade.| Tool: Use the automated test suite.| Test SIG  |
| Quality| Code|The project code complies with the community coding specifications and passes the code quality scanning.| Tool: Check whether the code can pass the community's basic quality check.| QA SIG  |
| Configuration management| Change control| The source code library of the project records all changes, including who modifies what and when. The source of all code is clearly recorded. The source of the code committed by contributors is recorded in detail.| Manual: Manually review code change logs.| QA SIG  |
| Configuration management|Version description|  A clear version change description is provided for each released version of the project, and the upgrade impact is specified, so that users can determine whether to perform the upgrade. If a release resolves security vulnerabilities, it lists all the disclosed vulnerabilities that have been fixed.| Manual: Review the release notes.|  Docs SIG|
| Configuration management| Version signature|  The version released by the project is digitally signed or has a hash digest to verify the integrity and reliability of a downloaded package.|  Tool + manual: Generate a hash value by referring to the guide and compare the generated hash value with the released hash value.| Infrastructure  SIG  |
| Configuration management| Version signature|  The source code is included in the release, and the standard, open packaging format is used during the release to ensure the readability in the long term.| Manual: Manually review the content of the release package.| Infrastructure  SIG  |
| Configuration management| Version signature|  The project release process is documented and can be repeated to generate a consistent release package.|  Tool + manual: Generate a hash value by referring to the guide and compare the generated hash value with the released hash value.| Infrastructure  SIG  |
| Quality| Security|The project uses secure and open encryption algorithms and protocols. It does not use encryption algorithms and protocols that have been cracked.| Tool: Use a security scanning tool to check whether the requirement is met.|  Security SIG |
| Quality| Security|The project uses cryptographically secure random number generators to generate all encryption keys and random numbers. It does not use cryptographically insecure generators.| Tool: Use a security scanning tool to check whether the requirement is met.|  Security SIG |
| Quality| Security|The project has already fixed vulnerabilities of the medium severity or higher that have been disclosed for more than 60 days. It also has fixed all critical vulnerabilities.| Tool: Use a security scanning tool to check whether the requirement is met.|  Security SIG |
